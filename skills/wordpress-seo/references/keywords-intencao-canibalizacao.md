# Keywords, intenção, canibalização, entidades e SEO para IA

## Classificação da página
Antes de otimizar, classifique: artigo informacional, página institucional, página de serviço, landing page, página comercial, produto, categoria/arquivo, página local, outro. Aplique as regras seguintes ajustadas ao tipo — regras de blog não se aplicam mecanicamente a produto/categoria/comercial.

## Intenção de busca
Classifique, quando aplicável: informacional, comercial investigativa, transacional, navegacional, local, híbrida. Considere também o estágio de jornada/funil quando isso ajudar a decisão (ex.: página de topo de funil não deve ser otimizada com copy de fundo de funil).

## Pesquisa de keyword em duas camadas

**Camada 1 — sempre disponível quando houver pesquisa web** (qualitativa): intenção, SERP, entidades, concorrentes, variações, long tails, perguntas, formatos, semântica. Ver `pesquisa-serp-concorrentes.md`.

**Camada 2 — só quando houver dado quantitativo confiável disponível** (fornecido pelo usuário ou por ferramenta real conectada): volume, tendência, sazonalidade, dificuldade, CPC, concorrência publicitária, outras métricas.

**Nunca inventar métricas da Camada 2.** Se volume, CPC, dificuldade ou tendência não estiverem disponíveis, diga isso explicitamente, não estime como se fosse dado real, e continue com a Camada 1. CPC pode funcionar como sinal comercial (indica intenção transacional/valor do clique), mas **não é fator de ranqueamento** — nunca o trate como se fosse. Nenhuma métrica isolada, de nenhuma camada, deve decidir sozinha a keyword principal — a decisão combina intenção, SERP, conteúdo, negócio, arquitetura e canibalização (abaixo).

## Frase-chave principal
Selecione com base em: intenção, SERP (ver `pesquisa-serp-concorrentes.md`), conteúdo real da página, objetivo de negócio, concorrência, arquitetura do site, risco de canibalização. **Não escolha uma keyword só porque parece semanticamente adequada** — valide contra a SERP e contra o que o site já possui.

Depois defina sinônimos/variações naturais da principal.

## Canibalização

Antes de criar uma URL nova, sempre pergunte: **esta intenção já possui uma URL no site?** Isso não é uma pergunta retórica — verifique operacionalmente, usando o que houver disponível:

- Sitemap XML do site.
- Busca interna do site (se acessível).
- Listagem de URLs/categorias/produtos/artigos já conhecida ou fornecida pelo usuário.
- Google Search Console (páginas que já recebem impressão para consultas relacionadas), quando disponível — ver `integrations/search-console.md`.
- Ferramentas de pesquisa web disponíveis na sessão (`site:dominio.com termo`).
- O `mapa-keywords-urls.md` já construído para o projeto, se existir.

Se nenhuma dessas fontes estiver disponível, diga isso explicitamente ao usuário e pergunte diretamente se já existe conteúdo sobre o tema — não assuma que não existe só porque não foi possível verificar.

Se a intenção já tiver URL, avalie nesta ordem:
1. Essa URL já atende bem à intenção? → considere **manter/atualizar** em vez de criar nova.
2. Precisa de mais profundidade? → **expandir**.
3. Há duas URLs competindo? → **consolidar** uma nas outras e redirecionar.
4. A intenção é genuinamente distinta (ainda que próxima)? → só então, criar nova página, com diferenciação clara de intenção e arquitetura (link entre elas).

Não crie múltiplas páginas para a mesma intenção sem essa verificação e justificativa explícita. Para uma visão em nível de site/cluster (não só a URL isolada), use `mapa-keywords-urls.md`.

## Entidades e SEO semântico
Mapeie, além das keywords:
- Entidades principais do tema.
- Conceitos relacionados que um especialista no assunto esperaria ver cobertos.
- Atributos e relações entre entidades.
- Subtemas necessários para cobertura completa.

SEO não se reduz a repetição de palavras-chave — cobertura semântica correta é o que sustenta tanto ranqueamento quanto citação por sistemas de IA.

## SEO para IA / respostas generativas (GEO)
Trate como consequência de conteúdo bem estruturado, não como "hack" à parte:
- Respostas claras e diretas para as perguntas centrais do tema.
- Entidades e relações explícitas no texto (não apenas implícitas).
- Fontes verificáveis e fatos checáveis.
- Autoria e estrutura semântica correta (headings, listas, tabelas onde fizer sentido).
- Precisão acima de tudo — informação incorreta prejudica tanto SEO tradicional quanto citação por IA.

Nunca venda isso como "truque" para o usuário — é resultado direto de conteúdo útil, factual e bem estruturado. **Nunca garanta** que isso fará a página ser citada em AI Overviews, ChatGPT, Gemini ou qualquer outro sistema — não há como prometer citação por um sistema de terceiros.
