# Core Web Vitals / Performance e Mobile SEO

## Core Web Vitals / Performance

Considere, quando houver dado real disponível (PageSpeed Insights, CrUX, Search Console):
- **LCP** (Largest Contentful Paint) — geralmente ligado a imagem/hero pesado, fontes bloqueantes, JS render-blocking.
- **INP** (Interaction to Next Paint) — geralmente ligado a JavaScript pesado (builders como Elementor, plugins acumulados).
- **CLS** (Cumulative Layout Shift) — geralmente ligado a imagens sem dimensão definida, fontes com FOUT/FOIT, banners/popups inseridos após o load.
- Imagens — peso, formato, dimensão declarada, lazy loading correto (ver `imagens-social.md`).
- Fontes — número de famílias/pesos carregados, `font-display`.
- JavaScript — plugins acumulados, scripts de terceiros (chat, pixels, analytics) carregados de forma bloqueante.
- Elementor especificamente — número de widgets/animações pode impactar INP; avaliar necessidade real de cada efeito.
- Cache — configuração de cache de página e CDN.

**Não invente métricas.** Se não houver dado medido, registre explicitamente como "não avaliado" (○, ver `checklist-final.md`) — nunca estime CWV de cabeça.

Ao comentar sobre performance, distinga sempre qual dos três níveis está sendo usado:

| Nível | Quando usar |
|---|---|
| **OBSERVAÇÃO** | Algo visível na página/código (ex.: "a imagem hero não tem `width`/`height` declarados") |
| **HIPÓTESE** | Dedução razoável a partir da observação, mas não medida (ex.: "isso provavelmente contribui para CLS") |
| **MÉTRICA MEDIDA** | Valor real de uma ferramenta (PageSpeed Insights, CrUX, Search Console) |

**Nunca concluir que uma página "tem problema de LCP/INP/CLS" só pela aparência** — isso é HIPÓTESE, não MÉTRICA MEDIDA, e deve ser comunicado como tal ao usuário.

## Mobile SEO

Avalie quando possível (idealmente com screenshot ou acesso à página em viewport mobile):
- Hierarquia visual se mantém clara em tela pequena.
- Legibilidade — tamanho de fonte e contraste adequados sem zoom.
- Botões e áreas de toque com tamanho suficiente (evitar elementos clicáveis colados).
- Tabelas — não devem quebrar o layout ou exigir scroll horizontal não intencional.
- Imagens — adaptadas ao viewport, sem cortar informação crítica.
- Popups/interstitials — não devem cobrir o conteúdo principal logo na entrada (penalizado pelo Google em mobile).
- Navegação — menu e busca acessíveis e utilizáveis em mobile.
- Conteúdo acima da dobra — a primeira tela deve comunicar do que se trata a página, não só um hero decorativo vazio.
- Experiência geral — o Google indexa mobile-first; a versão mobile é a que efetivamente conta para ranqueamento.
