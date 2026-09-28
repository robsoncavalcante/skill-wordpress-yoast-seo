# Mapa Keyword × URL

Permite trabalhar em nível de SITE e CLUSTER, não apenas página isolada — insumo direto para canibalização, arquitetura, clusters, links, novas oportunidades, conteúdo órfão, e priorização entre criar × atualizar.

## Estrutura conceitual (uma linha por URL relevante ao caso em análise)

```
URL
Tipo de página
Intenção
Keyword principal
Keywords relacionadas
Cluster
Pillar (sim/não, ou qual pillar pertence)
Conversão esperada
Status (publicado/rascunho/staging)
Indexável? (sim/não/motivo)
Observações
```

## Exemplo conceitual (formato — não hardcodar este exemplo em nenhuma lógica nem reutilizar o tema como padrão)

```
/blog/tipos-de-x/        → artigo      → informacional            → "tipos de x"        → cluster X → aponta para categoria
/categorias/x/           → categoria   → comercial investigativa  → "x para [uso]"       → cluster X → aponta para produtos
/produto/x-modelo-1/     → produto     → transacional             → "nome/modelo do x"   → cluster X → conversão = compra
```

Este exemplo serve só para ilustrar o conceito de mapeamento — construa o mapa real a partir das URLs efetivas do site do usuário.

## Como construir o mapa na prática

1. Levante as URLs relevantes ao caso (não precisa ser o site inteiro toda vez) — ver `fontes-e-evidencias.md` e a seção de detecção operacional de canibalização em `keywords-intencao-canibalizacao.md` para como obter essa lista (sitemap, busca interna, categorias, dados fornecidos pelo usuário, ferramentas disponíveis na sessão).
2. Para cada URL, preencha o que for observável (tipo, intenção aparente, keyword aparente pelo title/H1) — marque como "a confirmar" o que não puder ser inferido com segurança.
3. Use o mapa para responder, antes de criar ou mudar algo:
   - Esta intenção já tem dona? (canibalização)
   - Esta URL está órfã (sem links internos apontando para ela)?
   - Este cluster tem um pillar claro, ou está sem hub?
   - Existe uma keyword/intenção relevante sem nenhuma URL cobrindo (oportunidade)?
   - Entre duas URLs candidatas a atualizar vs. criar nova, qual prioridade faz mais sentido dado o mapa completo?

## Escopo e limites

- O mapa é construído sob demanda, para o escopo necessário ao caso (uma categoria, um cluster, um conjunto de URLs fornecido) — não é obrigatório mapear o site inteiro sempre.
- Não é armazenamento persistente da skill — é uma estrutura de trabalho dentro da conversa/projeto atual, a menos que o usuário peça explicitamente para exportá-la (ex.: como planilha) e mantê-la à parte.
- Dados de status/indexação vêm de evidência real (sitemap, Search Console, resposta HTTP) — nunca presuma indexação sem checar.
