# Integração opcional — Google Search Console (conceitual)

Agnóstica por padrão: se não houver acesso direto (API/MCP) ao Search Console na sessão, a skill trabalha com o que o usuário fornecer manualmente (export, print, texto colado) — ver `medicao-ciclo.md`.

**Marcação**: integração conceitual. Não assuma nomes de tool/endpoint específicos; se uma integração real estiver conectada, confirme as capacidades reais disponíveis antes de assumir que existem.

## O que, em conceito, uma integração deste tipo permitiria

- Consultar consultas, impressões, cliques, CTR e posição média de uma URL ou propriedade, por período.
- Comparar períodos para identificar queda/ganho.
- Verificar status de indexação real de uma URL (cobertura, exclusões, motivo).
- Verificar se o sitemap foi processado e sem erros.
- Solicitar reindexação de uma URL específica.

## Regras que continuam valendo com ou sem integração

- Solicitar indexação **não garante** indexação, não garante ranking, não substitui sitemap, não corrige problema técnico, e não substitui qualidade/arquitetura (ver `medicao-ciclo.md`). Deixe isso explícito ao usuário sempre que recomendar a ação, mesmo quando a integração automatiza o clique.
- Dados reais do Search Console superam hipóteses iniciais de keyword — se a integração trouxer dado contrariando a keyword principal hipotetizada no Brief, a decisão se ajusta ao dado, não o contrário.
- Sem dado real (via integração ou fornecido pelo usuário), nunca estime posição/CTR/impressões — marque como "não avaliado".
