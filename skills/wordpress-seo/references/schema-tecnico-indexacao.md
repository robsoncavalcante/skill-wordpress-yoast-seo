# Schema, SEO técnico e indexação

## Schema.org

O Schema deve representar o que a página **realmente é** — nunca escolha um tipo só por vantagem percebida no rich result.

Tipos comuns a avaliar: WebPage, Article, Product, Organization, Person, BreadcrumbList, FAQPage, HowTo, LocalBusiness, e outros conforme o tipo de página (ver `produtos-categorias-local.md` para Product/LocalBusiness).

**Detectar duplicidade** é obrigatório antes de configurar Schema no Yoast — verifique se o mesmo grafo/entidade já é gerado por:
- Yoast (graph automático)
- WooCommerce (Schema de produto)
- Elementor (Pro, temas com Schema embutido)
- JetEngine / outros plugins de custom post type
- Tema
- Código customizado (functions.php, plugin próprio)

Schema duplicado, redundante ou conflitante pode gerar ambiguidade para os buscadores, dificultar validação e complicar manutenção futura — evite-o, mas trate isso como risco técnico a mitigar, não como uma regra absoluta tipo "duplicado é sempre pior que ausente" (depende do tipo de duplicidade e de quanto os grafos conflitam entre si).

Antes de adicionar Schema, identifique qual sistema é a **fonte de verdade** para aquele tipo de dado (Yoast, WooCommerce, Elementor, JetEngine, tema, ou código customizado) e evite que dois sistemas gerem o mesmo tipo de entidade de forma divergente. Quando o Yoast já gera automaticamente um graph consistente (WebPage/Organization/BreadcrumbList), não sobreponha com JSON-LD manual sem necessidade real.

Para produtos regulados (YMYL), o Schema deve refletir exatamente o que a Advanced/E-E-A-T/compliance permite afirmar — nunca "enriquecer" o Schema com alegações não sustentadas no conteúdo visível.

## Indexação e SEO técnico

Quando aplicável, verifique:
- HTTP status da URL (200, redirects em cadeia, 404/410).
- `robots.txt` — bloqueio acidental de diretórios relevantes.
- Meta robots (index/noindex, follow/nofollow) na própria página.
- Canonical — self-referencing por padrão, manual só com justificativa.
- Sitemap XML — a URL está incluída? Está atualizado?
- HTTPS ativo e sem mixed content.
- Redirects — existência, tipo (301 vs 302) e cadeias desnecessárias.
- Duplicidade de conteúdo e parâmetros de URL não canonicalizados.
- Paginação (rel next/prev não é mais sinal oficial do Google, mas a arquitetura de paginação ainda precisa ser saudável para indexação).
- Ambiente: **staging vs produção** — confirme sempre qual ambiente está sendo avaliado.

**Verificação crítica**: detecte especialmente ambientes com **noindex global** (comum em staging, ou em sites recém-migrados que esqueceram de desmarcar "Discourage search engines" no WordPress). Uma página configurada como `index` no Yoast pode continuar não indexável se o site inteiro estiver bloqueado em Settings → Reading, ou por regra no `robots.txt`, ou por header HTTP `X-Robots-Tag`. Sempre confira esses três níveis antes de diagnosticar um problema de indexação só pela página individual.

## Baseline de configuração (ver também `yoast-premium.md` → Advanced)

Index = sim · Follow = sim · Meta robots avançado = vazio salvo necessidade · Canonical = automática salvo justificativa · Breadcrumb = avaliar versão curta.
