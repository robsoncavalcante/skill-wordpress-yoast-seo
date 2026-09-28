# Yoast SEO Premium — configuração e interpretação

Comportamento específico de versão do plugin muda com o tempo. Se o usuário citar um comportamento que parece divergir do descrito aqui, ou a versão for recente, pesquise a documentação oficial do Yoast antes de afirmar algo com certeza.

## Frase principal e frases relacionadas

**Sinônimo ≠ frase-chave relacionada.**
- Sinônimo: outra forma linguística de representar essencialmente o mesmo conceito da frase principal.
- Frase-chave relacionada: consulta secundária com intenção compatível e cobertura **real** dentro da mesma página.

O Yoast Premium permitir várias frases relacionadas é **capacidade, não meta**. Não preencha todos os campos só porque existem.

Antes de cadastrar uma relacionada, avalie:
- A intenção é compatível com a página?
- Há cobertura real do subtema dentro do conteúdo (não forçada)?
- É natural, sem repetição artificial?
- Há risco de canibalização (a relacionada merecer página própria)?

Se otimizar uma relacionada exige repetições artificiais, **aceite o alerta do Yoast** e registre a decisão.

Prioridade sempre: **principal > cobertura semântica > relacionadas > pontuação do plugin.**

Cada frase relacionada pode ter seus próprios sinônimos e sua própria análise de legibilidade/SEO — trate cada uma com o mesmo rigor da principal, sem inflar o número de frases por padrão.

## SEO Title, H1 e Social Title

Três elementos com funções diferentes — podem ser diferentes entre si:
- **H1**: função editorial e hierárquica dentro da página.
- **SEO Title**: pensado para a SERP — intenção e relevância de clique.
- **Social Title**: pensado para compartilhamento e interesse no feed.

Não altere o H1 só para o Yoast ficar verde quando isso prejudicar a qualidade editorial.

## Slug

**Conteúdo novo**: curto, legível, descritivo, alinhado à intenção, sem palavras desnecessárias. Antes de definir, verifique se o slug já existe e se a intenção já é atendida por outra URL.

**Conteúdo publicado**: nunca recomende alteração automaticamente. Avalie primeiro as consequências (indexação, backlinks, histórico) e a necessidade de redirect 301.

## Meta description

Deve: representar corretamente a página, incluir a frase-chave quando natural, comunicar benefício/informação real, evitar clickbait e keyword stuffing, respeitar como aparece na SERP.

Não trabalhe apenas com contagem rígida de caracteres — considere a largura/renderização quando o Yoast fornecer essa informação (preview de pixels).

## Imagens e social — campos específicos
Ver `imagens-social.md` para ALT, Open Graph, dimensões e quando diferenciar campos de X/Twitter da configuração social geral (só quando houver razão para diferenciar).

## Schema (aba Schema do Yoast)
Ver `schema-tecnico-indexacao.md` — atenção especial a duplicidade entre Yoast e WooCommerce/Elementor/JetEngine/tema/código customizado.

## Advanced (aba Advanced do Yoast)

Baseline para artigo indexável padrão:
- Index = sim (Allow search engines to show this Page in search results = Yes)
- Follow = sim
- Meta robots avançado = vazio, salvo necessidade específica (ex.: noimageindex em página com imagens de terceiros)
- Canonical URL = automática (campo vazio), salvo justificativa explícita para canonical manual
- Breadcrumb title = avaliar uma versão curta quando o título completo quebra o breadcrumb visualmente

**Nunca preencha canonical manualmente só porque o campo existe.**

## Interpretando prints do Yoast enviados pelo usuário

Ao receber um screenshot da análise do Yoast, classifique cada item observado em uma das quatro categorias — não trate tudo como "erro":

| Categoria | O que é |
|---|---|
| **ERRO TÉCNICO** | Algo objetivamente quebrado (ex.: página sem H1, meta description vazia sem intenção) |
| **RECOMENDAÇÃO** | Sugestão do plugin que pode ou não fazer sentido para o caso |
| **OPORTUNIDADE** | Algo que melhoraria a página sem trade-off relevante |
| **ALERTA ACEITO / DECISÃO CONSCIENTE** | Vermelho/laranja mantido de propósito, com justificativa registrada |

Vermelho não é sinônimo de erro real. Explique ao usuário a diferença antes de recomendar qualquer ação sobre o print.
