# Particularidades WordPress / Elementor / JetEngine / WooCommerce

Este arquivo cobre comportamento de plataforma que afeta decisões de SEO mas não é, em si, estratégia de SEO. Comportamento de plugin muda por versão — se algo parecer desatualizado, pesquise a documentação oficial do plugin/tema antes de afirmar com certeza.

**Não assuma o stack.** WordPress puro (tema clássico ou block editor/Gutenberg), Elementor, WooCommerce e JetEngine são plugins/builders independentes — nem todo WordPress usa Elementor, nem todo Elementor usa WooCommerce ou JetEngine. Antes de aplicar qualquer orientação abaixo, confirme (via `contexto-negocio-site.md`, inspeção da página, ou pergunta direta se não houver como inferir) qual stack está realmente em uso, e adapte a análise — não aplique as seções de Elementor/JetEngine/WooCommerce a um site que não os usa.

## Risco geral de duplicação entre plugins/tema

Quando múltiplos plugins ou o tema implementam a mesma função, o risco de duplicidade/conflito existe em: **title**, **canonical**, **Schema**, **breadcrumbs**, **Open Graph**, **meta robots**. Antes de configurar qualquer um desses campos no Yoast, verifique se o tema ou outro plugin já está gerando o mesmo campo (ex.: tema com SEO embutido, outro plugin de SEO ativo simultaneamente, builder com Open Graph próprio) — dois sistemas competindo pelo mesmo campo é uma causa comum de comportamento inconsistente que não aparece como "erro" óbvio.

## WordPress core
- `Settings → Reading → Discourage search engines from indexing this site` — sempre confira este checkbox antes de diagnosticar problema de indexação; é a causa mais comum de "index=yes no Yoast mas não indexa" (ver `schema-tecnico-indexacao.md`).
- Estrutura de permalinks afeta slug e arquitetura de categoria — mudança de estrutura em site publicado exige plano de redirect completo, não só ajuste pontual.
- Revisões e rascunhos não devem ser indexáveis; confirme que `/?p=123` e URLs de preview não vazam para o índice.

## Elementor / Elementor Pro
- Texto inserido via widgets de Elementor (Text Editor, Heading) é o que o Yoast analisa — conteúdo dentro de widgets não padrão (sliders, carrosséis, templates dinâmicos) pode não ser lido corretamente pela análise de conteúdo do Yoast; verifique com o preview de conteúdo do plugin.
- Um H1 duplicado é comum quando o tema já renderiza H1 do título do post E o template Elementor adiciona outro H1 no Hero — sempre audite quantos H1 existem na página renderizada, não só no editor.
- Templates de Elementor (headers, footers, arquivos de loop) podem introduzir texto/links repetidos em massa em todas as páginas — cuidado ao avaliar "conteúdo único" de uma página que na verdade importa muito conteúdo de template global.

## JetEngine / custom post types e taxonomias
- Custom post types precisam ter sua própria configuração de Yoast (title/description templates) — confirme que o CPT não está usando o template genérico de "Post" sem ajuste.
- Taxonomias customizadas (JetEngine, ACF, etc.) geram arquivos que também precisam de decisão de indexação (ver `produtos-categorias-local.md`).
- Campos dinâmicos (JetEngine Meta Box) usados no title/H1 via macros — confirme que o Yoast está lendo o valor renderizado, não a macro em si, ao avaliar a análise de keyword.

## WooCommerce
- WooCommerce gera Schema de produto próprio — checar duplicidade com o Schema do Yoast é obrigatório (ver `schema-tecnico-indexacao.md`).
- Página de categoria de produto (`product_cat`) e a página de loja (`Shop`) têm regras de indexação próprias — decida deliberadamente se cada uma deve ser indexável (ver `produtos-categorias-local.md`).
- Variações de produto normalmente não devem gerar URLs indexáveis próprias — confirme que a configuração de canonical do produto-pai está correta.

## Cache e CDN
- Antes de validar qualquer mudança de SEO em produção, confirme que o cache de página/CDN foi limpo — um teste que parece "não aplicado" às vezes é só cache servindo versão antiga.
