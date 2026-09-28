# Contexto de negócio e site

Etapa que antecede (ou acompanha) a decisão CRIAR × OTIMIZAR. Objetivo: entender o suficiente de

```
NEGÓCIO → SITE → MERCADO → PÚBLICO → TIPO DE PÁGINA → OBJETIVO → CONVERSÃO → INTENÇÃO DE BUSCA
```

antes de qualquer recomendação estratégica — sem virar interrogatório.

## O que a skill precisa saber, quando for relevante à decisão

- Empresa/marca
- Domínio
- País e idioma
- Mercado / segmento
- Produto ou serviço
- Público-alvo
- Área geográfica de atuação (se local)
- Objetivo do site como um todo
- Objetivo específico da URL em questão
- Conversão esperada dessa URL
- Estágio do site: desenvolvimento, staging, produção, migração em andamento
- Concorrentes conhecidos (se o usuário já tiver)
- CMS (assume-se WordPress, mas confirme variações relevantes)
- Plugin de SEO em uso (assume-se Yoast Premium — confirme se for outro)
- Elementor / JetEngine / WooCommerce / outros builders ou plugins relevantes
- Qualquer outra característica que mude a estratégia (ex.: multi-idioma, multi-site, marketplace)

## Regra fundamental: nunca interrogatório

**Não pergunte o que já pode ser inferido com segurança** a partir de:
- URL fornecida (domínio, estrutura, idioma aparente, país no ccTLD)
- Conteúdo já compartilhado (produto, tom, público implícito)
- Briefing do usuário
- Dados já fornecidos na conversa (mesmo em mensagens anteriores)
- Ferramentas disponíveis na sessão (ex.: ler a home do site para entender negócio/mercado)

Pergunte **somente** o que:
1. Realmente muda a decisão SEO a ser tomada agora, e
2. Não pode ser obtido de outra forma disponível.

Exemplo: se o usuário já colou a URL de um site de suplementos brasileiro, não pergunte "qual é o mercado" nem "qual país" — infira e confirme brevemente se houver ambiguidade, em vez de abrir um formulário de perguntas.

## Como usar o contexto levantado

- Alimenta a classificação de página e intenção (`keywords-intencao-canibalizacao.md`).
- Determina se o gate de compliance/YMYL deve ativar (`eeat-ymyl-compliance.md`).
- Determina se SEO Local se aplica (`produtos-categorias-local.md`).
- Informa o `brief-seo.md` antes da redação de conteúdo novo.
- Informa quais particularidades de stack revisar (`wordpress-elementor.md`).

## Persistência

Este contexto não é salvo automaticamente entre sessões — é levantado (ou confirmado) na conversa atual. Se o usuário quiser que ele persista entre sessões/projetos, isso depende de um mecanismo de memória externo à skill (ex.: um arquivo de projeto que o próprio usuário mantém) — não assuma que a skill "lembra" de uma sessão para a outra.
