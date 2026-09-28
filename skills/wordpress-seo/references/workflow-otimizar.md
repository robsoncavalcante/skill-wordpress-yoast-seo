# Workflow — Otimizar conteúdo existente

Sequência: **contexto → auditoria → SERP → gaps → preservação do que funciona → alterações necessárias → SEO → Yoast**.

## 0. Contexto
- Carregue `contexto-negocio-site.md` se ainda não tiver esse pano de fundo — sem repetir perguntas já respondidas na conversa.

## 1. Levantamento inicial (obrigatório antes de recomendar qualquer mudança)
- URL, status de publicação, indexação atual, idade aproximada, objetivo de negócio.
- Dados de desempenho disponíveis (Search Console, GA4, rankings) — se o usuário tiver, peça; se não, prossiga qualitativamente.
- Histórico de alterações relevantes (redesigns, mudanças de slug, penalizações, picos/quedas conhecidos).
- Backlinks e links internos existentes apontando para a URL — mudanças estruturais (slug, H1, canonical, intenção) só depois de considerar o impacto nesses pontos e a necessidade de redirect 301.

**Nunca recomende mudança de slug/URL publicada apenas para satisfazer um indicador do Yoast.**

## 2. Auditoria de conteúdo
- Leia/recupere a página (via URL, se houver acesso web).
- Classifique tipo de página e intenção atual servida — confirme que ainda é a intenção correta (a SERP pode ter mudado).
- Rode `pesquisa-serp-concorrentes.md` para comparar com a SERP atual.

## 3. Content Decay — sinais a verificar
- Informação desatualizada (dados, preços, regulamentação, produtos descontinuados).
- SERP mudou de formato (ex.: passou a exigir vídeo, tabela, FAQ) ou de intenção dominante.
- Links quebrados (internos e externos).
- Estatísticas/citações antigas sem atualização.
- Novas entidades relevantes ao tema que surgiram.
- Perda de desempenho mensurável (se houver dado de Search Console/GA4).

## 4. Decisão (cada uma exige justificativa registrada em `decision-log.md`)
- **MANTER** — está atendendo bem, mudança traria risco sem ganho.
- **ATUALIZAR** — dados/exemplos/seções pontuais desatualizados; estrutura e intenção continuam corretas.
- **EXPANDIR** — intenção coberta parcialmente; faltam subtemas que a SERP/concorrência demonstram ser esperados.
- **CONSOLIDAR** — duas ou mais URLs competem pela mesma intenção (canibalização); fundir em uma e redirecionar as demais.
- **REDIRECIONAR** — a URL não tem mais razão de existir isoladamente; 301 para a página que melhor atende à intenção.
- **REMOVER** — conteúdo obsoleto sem equivalente, sem valor de negócio nem histórico de tráfego relevante a preservar.

## 5. O que preservar por padrão
- URL/slug já indexado e com backlinks, salvo justificativa forte + plano de redirect.
- H1 e frase-chave principal se ainda representam a intenção corretamente.
- Estrutura de links internos que já aponta para a página.

## 6. Aplicar mudanças
- Priorize o que move a agulha na intenção e na cobertura semântica antes de mexer em campos do Yoast.
- Reavalie frases relacionadas, meta description, Schema e Advanced conforme `yoast-premium.md` e `schema-tecnico-indexacao.md` — só altere o que tem motivo real.
- Replaneje links internos/reversos — `links-clusters.md`.

## 7. Fechar
- Gere `checklist-final.md` e, se aplicável, agende reavaliação em `medicao-ciclo.md` (ciclo CRIAR→PUBLICAR→MEDIR→DIAGNOSTICAR→ATUALIZAR→MEDIR NOVAMENTE).
- Aplique a stop condition do `SKILL.md` — pare quando os pontos críticos estiverem resolvidos, mesmo que restem oportunidades teóricas menores.
