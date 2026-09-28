# Protocolo de fontes e evidências

Hierarquia adaptável de confiabilidade — a ordem exata muda conforme o assunto, mas o princípio de rigor crescente para temas sensíveis é constante.

## Hierarquia geral

1. Fonte primária/oficial (o próprio órgão, empresa, autor original do dado)
2. Documentação técnica oficial (ex.: Google Search Central, Schema.org, documentação oficial do Yoast/WordPress)
3. Literatura científica (revisada por pares, quando o tema exigir)
4. Instituições reconhecidas (universidades, órgãos setoriais estabelecidos)
5. Fontes secundárias qualificadas (jornalismo especializado, análises técnicas de terceiros confiáveis)
6. Comunidade/opinião — só quando o objetivo da pesquisa exigir percepção, experiência prática ou sentimento (ex.: "o que profissionais da área comentam sobre X"), nunca como base factual isolada

## Quando elevar o rigor

Para fatos técnicos, jurídicos, médicos, regulatórios ou qualquer tema YMYL (ver `eeat-ymyl-compliance.md`): suba direto para os níveis 1-3 e evite basear qualquer afirmação nos níveis 5-6. Concorrentes e blogs genéricos de SEO **nunca** substituem fonte primária nesses casos.

## Classificação obrigatória de toda afirmação não trivial

Ao apresentar uma informação que não seja senso comum óbvio, classifique-a (mentalmente, e explicitamente quando o caso for sensível):

| Rótulo | Significa |
|---|---|
| **CONFIRMADO** | Verificado em fonte primária/oficial atual |
| **SUSTENTADO POR EVIDÊNCIA** | Apoiado por fonte secundária qualificada ou por dado concreto observado (ex.: Search Console do próprio usuário) |
| **INFERIDO** | Deduzido logicamente a partir de evidência indireta (ex.: "a SERP sugere que...") |
| **HIPÓTESE** | Suposição razoável sem verificação — deve ser dita como tal |
| **NÃO VERIFICADO** | Não foi possível checar; usar com essa ressalva explícita |

**Nunca apresentar uma inferência ou hipótese como se fosse fato confirmado.** Isso vale especialmente para: alegações de produto, dados regulatórios, comportamento de plugin/algoritmo, e qualquer métrica quantitativa (volume, CPC, dificuldade — ver `keywords-intencao-canibalizacao.md`).

## Relação com outros módulos

- `pesquisa-serp-concorrentes.md` usa este protocolo para não tratar concorrente como fonte factual.
- `eeat-ymyl-compliance.md` usa este protocolo para decidir o que pode ser afirmado sem comprovação.
- `keywords-intencao-canibalizacao.md` usa este protocolo para as duas camadas de pesquisa de keyword (qualitativa sempre disponível vs. quantitativa só quando há dado real).
