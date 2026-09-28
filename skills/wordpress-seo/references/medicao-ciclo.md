# Search Console, GA4, pós-publicação e ciclo contínuo

## Search Console

Quando o usuário fornecer dados (export, print ou acesso), analise:
- Consultas que geram impressões/cliques para a URL.
- Impressões, cliques, CTR e posição média — e a evolução no tempo, não só o snapshot.
- Páginas com queda ou ganho relevante.
- Consultas com alta impressão e baixo CTR (oportunidade de melhorar title/meta description).
- Consultas com boa posição e baixo volume (oportunidade de expandir cobertura).

**Dados reais superam hipóteses iniciais de keyword.** Se o Search Console mostra que a página já rankeia bem para uma consulta diferente da hipótese inicial, ajuste a estratégia para essa evidência real, não o contrário.

## GA4 / Conversão

SEO não termina no ranking. Identifique o KPI da página antes de recomendar qualquer mudança:
- Lead / formulário
- Venda / checkout
- WhatsApp / contato direto
- Download
- Clique para produto/serviço
- Outra conversão específica do negócio

Toda recomendação de mudança (copy, CTA, estrutura) deve considerar o objetivo real da página, não só métricas de tráfego. Uma página pode ganhar tráfego e perder conversão — isso é regressão, não sucesso.

## Checklist pós-publicação

Ao publicar (novo ou republicar existente), confirme:
- URL correta e final (sem `-2`, sem parâmetros acidentais).
- Status = publicado (não agendado/rascunho por engano).
- Indexabilidade — index/follow corretos e sem bloqueio global (ver `schema-tecnico-indexacao.md`).
- Sitemap XML — URL presente.
- Canonical correto.
- Schema válido (testar em ferramenta de teste de dados estruturados quando possível).
- Links — internos funcionando, sem 404.
- Imagens — carregando, ALT presente, peso adequado.
- Social — preview de Open Graph correto.
- Mobile — renderização adequada.
- Performance — sem regressão perceptível.
- Search Console — solicitar indexação se for urgente (ver ressalva abaixo).
- Acompanhamento agendado (ver ciclo abaixo).

**Solicitar indexação no Search Console**: se recomendar essa ação, deixe explícito para o usuário que ela **não garante indexação, não garante ranking, não substitui o sitemap, não corrige problema técnico e não substitui qualidade ou arquitetura**. É um pedido de rastreamento prioritário, não uma solução para o que estiver causando a não-indexação.

## Ciclo contínuo

```
CRIAR → PUBLICAR → MEDIR → DIAGNOSTICAR → ATUALIZAR → MEDIR NOVAMENTE
```

Sempre que fechar uma URL, registre quando ela deve ser reavaliada (ex.: "checar Search Console em 4-6 semanas") — isso não é uma tarefa automática da skill, é um lembrete a deixar explícito para o usuário, já que o acompanhamento depende de dados que só ele tem acesso (ou de uma integração opcional — ver `integrations/search-console.md` e `integrations/ga4.md`).

A próxima revisão deve ser orientada por dados reais sempre que eles existirem: se o Search Console/GA4 mostrar um padrão diferente do previsto no Brief original (`brief-seo.md`), a hipótese inicial cede à evidência — não o contrário.
