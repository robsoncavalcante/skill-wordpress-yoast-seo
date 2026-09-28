# Exemplos de fluxo ponta a ponta

Estes exemplos ilustram como a skill deve se comportar na prática, sem despejar tudo de uma vez. São genéricos — não copiar nomes de projeto, nicho ou marca de exemplos anteriores para dentro de um novo caso real.

## 1. Artigo informacional novo

1. Usuário dá o tema (mesmo que seja só "quero escrever sobre X"). Skill infere o que der de `contexto-negocio-site.md` e só pergunta o que realmente falta — não abre formulário.
2. Carrega `pesquisa-serp-concorrentes.md` → identifica intenção dominante e subtemas recorrentes (Camada 1 de `keywords-intencao-canibalizacao.md`).
3. Carrega `keywords-intencao-canibalizacao.md` → checa operacionalmente se o site já tem URL para essa intenção (sitemap/busca interna/mapa). Se não, segue.
4. Monta o SEO Brief (`brief-seo.md`), ao menos internamente.
5. Propõe outline (H1/H2/H3) com base na pesquisa — uma etapa por vez, não o artigo inteiro ainda.
6. Após aprovação do outline, redige o conteúdo diretamente no chat (sem tags `<p>`, o WordPress/Elementor insere parágrafo automaticamente — só usar heading tags quando necessário).
7. Aplica `yoast-premium.md` — propõe frase principal, SEO Title, meta description, e só sugere frase relacionada se houver cobertura real.
8. Propõe links internos/externos (`links-clusters.md`) e Schema (`schema-tecnico-indexacao.md`).
9. Entrega checklist final (`checklist-final.md`) e aplica a stop condition do `SKILL.md`.

## 2. Artigo existente (auditoria)

1. Usuário fornece a URL. Skill recupera a página (se houver acesso web) e pergunta objetivo/dados de desempenho disponíveis.
2. Carrega `workflow-otimizar.md` → levantamento inicial (indexação, idade, histórico).
3. Compara com a SERP atual (`pesquisa-serp-concorrentes.md`) → identifica se a intenção mudou ou se há gap de cobertura.
4. Verifica sinais de content decay.
5. Recomenda UMA decisão por vez (manter/atualizar/expandir/consolidar/redirecionar/remover) com justificativa — não despeja a lista inteira de possíveis mudanças de uma vez.
6. Aplica mudanças aprovadas, revisando Yoast só nos campos que realmente precisam mudar.
7. Registra decisões relevantes em `decision-log.md`.

## 3. Página comercial/serviço

1. Classifica como página comercial (não artigo) — outline e copy voltados a intenção comercial investigativa/transacional, não didática.
2. Pesquisa SERP com foco em como concorrentes estruturam a oferta (não só conteúdo educativo).
3. CTA e prova social (E-E-A-T) ganham peso maior que densidade de keyword.
4. Schema tipicamente Service/LocalBusiness/Organization conforme o caso — checar duplicidade com tema/builder.
5. Links internos priorizam converter para contato/proposta, não só "ler mais".

## 4. Produto (e-commerce)

1. Carrega `produtos-categorias-local.md` → fluxo de produto.
2. Confirma se o setor é regulado → se sim, `eeat-ymyl-compliance.md` antes de qualquer copy.
3. Descrição original (nunca copiar do fabricante), atributos, Product Schema sem duplicar WooCommerce.
4. Links para conteúdo educacional relacionado do cluster e produtos relacionados reais.
5. Checklist final adaptado (ex.: "Conversão" vira métrica central).

## 5. Categoria

1. Carrega `produtos-categorias-local.md` → decide indexar ou não.
2. Se indexável, propõe texto introdutório único (evitar thin content).
3. Avalia se a categoria deve funcionar como hub de cluster (`links-clusters.md`).
4. Verifica duplicidade com tags/outras categorias.

## 6. Análise URL própria × concorrente

1. Usuário fornece a própria URL e uma ou mais URLs de concorrentes.
2. Carrega `pesquisa-serp-concorrentes.md` → decompõe cada página nos critérios definidos, sem copiar texto/estrutura autoral.
3. Monta a matriz NOSSA × CONCORRENTE A × CONCORRENTE B × SERP.
4. Propõe o que cobrir para ficar mais completo, útil e confiável — nunca "copiar o que o concorrente fez".
5. Se a própria URL já existe, segue para `workflow-otimizar.md` com os gaps identificados como insumo.

## 7. YMYL / compliance (ex.: suplemento, saúde, financeiro)

1. Detecta o gatilho YMYL já na classificação inicial da página.
2. Carrega `eeat-ymyl-compliance.md` **antes** de qualquer redação — levanta o que pode/não pode ser afirmado.
3. Redige com E-E-A-T reforçado: autoria, fontes primárias/reguladoras, sem promessa terapêutica ou alegação não sustentada.
4. Revisa novamente depois da redação, checando se alguma otimização de SEO (título chamativo, keyword "forte") introduziu alegação problemática.
5. Sinaliza explicitamente ao usuário qualquer afirmação que exigiria comprovação não fornecida — nunca inventa essa comprovação.
6. Checklist final marca a linha "Compliance" com o que foi de fato verificado, não um ✓ genérico.
