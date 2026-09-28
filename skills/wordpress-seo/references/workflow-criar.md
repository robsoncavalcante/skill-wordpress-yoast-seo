# Workflow — Criar conteúdo novo

Sequência: **contexto → pesquisa → SEO Brief → arquitetura → outline → redação → revisão → SEO → Yoast**.

## 0. Contexto
- Carregue `contexto-negocio-site.md` — só o suficiente para decidir a estratégia (não interrogatório). Se o usuário só disse "quero escrever sobre X", esse é o momento de inferir o que der e perguntar apenas o que realmente falta.

## 1. Pesquisa
- Se houver tema/briefing mas não URL, entenda o objetivo de negócio da página antes de qualquer keyword.
- Carregue `pesquisa-serp-concorrentes.md` para entender a SERP atual antes de definir estratégia.
- Carregue `keywords-intencao-canibalizacao.md` para classificar intenção e checar se a intenção já tem URL no site (canibalização) — use a detecção operacional descrita lá (sitemap, busca interna, `mapa-keywords-urls.md`) antes de concluir que não há conflito. Não crie página nova para intenção já atendida sem essa verificação.

## 1.5 SEO Brief
- Antes de ir para outline/redação, monte o Brief conforme `brief-seo.md` — mesmo que não seja exibido por inteiro ao usuário, ele organiza o que a pesquisa já levantou e evita retrabalho na redação.

## 2. Arquitetura
- Classifique o tipo de página (artigo, institucional, serviço, landing, comercial, produto, categoria, local) — ver `SKILL.md`.
- Decida se a página é cornerstone/pilar de um cluster ou um cluster de um pilar existente — ver `links-clusters.md`. Não marque cornerstone só por o artigo ser longo.
- Defina slug: curto, legível, descritivo, alinhado à intenção, sem palavras desnecessárias. Verifique antes se o slug já existe ou se a intenção já é atendida por outra URL.

## 3. Outline
- Estruture H1 único, H2/H3 cobrindo subtemas identificados na pesquisa de SERP/concorrentes.
- Mapeie entidades e conceitos relacionados (não apenas palavras-chave) — ver seção "Entidades" em `keywords-intencao-canibalizacao.md`.
- Planeje onde entram: FAQ (só se perguntas reais merecerem), tabelas/listas/definições candidatas a featured snippet, CTA, mídia.

## 4. Redação
- Linguagem natural, sem keyword stuffing.
- Priorize responder de forma clara e verificável — estrutura que facilita compreensão por buscadores e sistemas de IA é consequência de conteúdo bem estruturado e factual, não um "hack de GEO" à parte.
- Se o tema for YMYL, aplique `eeat-ymyl-compliance.md` **antes** de redigir (restrições de alegação) e novamente depois (revisão).

## 5. Revisão editorial
- Releia por precisão, utilidade, naturalidade e UX antes de qualquer ajuste de SEO.
- Confirme H1, SEO Title e Social Title como elementos distintos (podem divergir) — ver `yoast-premium.md`.

## 6. SEO
- Frase-chave principal definida com base em intenção + SERP + conteúdo + negócio + arquitetura do site + risco de canibalização (não só "parece semanticamente adequada").
- Planeje links internos de saída (para páginas relevantes existentes) e links reversos (quais páginas antigas devem passar a apontar para esta) — `links-clusters.md`.
- Links externos apenas com função editorial real, priorizando fontes primárias — `links-clusters.md`.
- Imagens: filename, ALT descritivo (não depósito de keyword), compressão, formato, imagem destacada — `imagens-social.md`.
- Schema correspondente ao que a página realmente é, checando duplicidade com WooCommerce/Elementor/JetEngine/tema — `schema-tecnico-indexacao.md`.

## 7. Yoast
- Configure frase principal e, só se fizer sentido, frases relacionadas — critérios em `yoast-premium.md`.
- Configure SEO Title, meta description, social — `yoast-premium.md`.
- Advanced: index=sim, follow=sim, meta robots avançado vazio salvo necessidade, canonical automática salvo justificativa — `schema-tecnico-indexacao.md`.
- Aceite conscientemente alertas do Yoast quando a alternativa prejudicar naturalidade/precisão; registre em `decision-log.md`.

## 8. Publicação
- Ao publicar, carregue `medicao-ciclo.md` para o checklist pós-publicação e o ciclo de monitoramento.
