# SEO de produto, categorias/taxonomias e SEO local

## SEO de produto

Fluxo específico — não trate produto como artigo de blog:
- Nome do produto alinhado à forma como o público realmente busca (nem sempre o nome comercial "criativo").
- Intenção: majoritariamente transacional/comercial investigativa — a copy deve responder isso primeiro.
- Descrição **original** — nunca copiar texto de fabricante/distribuidor sem reescrita real (risco de conteúdo duplicado entre múltiplos revendedores do mesmo produto).
- Atributos, composição e informações relevantes completos e verificáveis.
- Imagens: múltiplos ângulos, ALT descritivo, otimização de peso — ver `imagens-social.md`.
- Product Schema — completo (nome, descrição, imagem, marca, oferta/preço/disponibilidade quando aplicável) e sem duplicar o que WooCommerce já gera (ver `schema-tecnico-indexacao.md`).
- Categoria correta e única fonte de verdade para o produto.
- Links para conteúdo educacional relacionado (cluster) e produtos relacionados relevantes (não aleatórios).
- Canonical — confirmar que variações não geram páginas concorrentes com o produto principal.
- Informações comerciais aplicáveis (disponibilidade, condições) mantidas atualizadas — dados estruturados inconsistentes com o conteúdo/estado real da página (ex.: Schema dizendo "em estoque" quando não está) podem gerar erros de validação, problemas de qualidade e inelegibilidade para determinados resultados enriquecidos; não chame isso automaticamente de "penalização" sem essa ser a terminologia oficial do caso.

Em setores regulados, execute `eeat-ymyl-compliance.md` antes de finalizar qualquer copy de produto.

## Categorias, tags e taxonomias

Para cada taxonomia, decida deliberadamente:
- **Indexar ou não** — uma tag ou categoria só deve ser indexável se tiver valor de busca próprio (não é padrão indexar tudo).
- **Conteúdo próprio** — a página tem texto introdutório único, ou é só uma lista de posts (thin content)?
- **Duplicação** — a mesma intenção já é atendida por outra categoria, tag ou página?
- **Relação com clusters** — a categoria pode funcionar como hub de um topic cluster (ver `links-clusters.md`)?
- **Links internos** — a categoria recebe e distribui links de forma coerente com sua importância?

Categorias estratégicas podem e devem funcionar como hubs — trate-as com o mesmo cuidado editorial de uma página cornerstone quando isso fizer sentido.

## SEO Local

Ative apenas quando o negócio realmente tiver relevância local (atendimento físico, área de atuação geográfica, etc.).

Avalie:
- **NAP** (Name, Address, Phone) consistente em todo o site e alinhado ao Google Business Profile.
- Necessidade de páginas regionais (por cidade/região) — só crie se houver conteúdo genuinamente distinto por região (oferta, contato, equipe local); páginas idênticas trocando apenas o nome da cidade são **doorway pages** e são um risco, não uma estratégia.
- Intenção local explícita no conteúdo (não apenas no title).
- Schema LocalBusiness quando aplicável, com dados NAP consistentes com o resto do site.
- Sinal de proximidade/área de cobertura clara para o usuário e para o buscador.
