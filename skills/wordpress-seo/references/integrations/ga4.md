# Integração opcional — GA4 (conceitual)

Agnóstica por padrão: sem acesso direto (API/MCP) ao GA4 na sessão, a skill trabalha com o que o usuário fornecer manualmente — ver `medicao-ciclo.md`.

**Marcação**: integração conceitual. Não assuma nomes de tool/endpoint específicos; se uma integração real estiver conectada, confirme as capacidades reais disponíveis antes de assumir que existem.

## O que, em conceito, uma integração deste tipo permitiria

- Consultar sessões, usuários, taxa de engajamento e eventos de conversão por página/período.
- Identificar o KPI de conversão configurado para a página (lead, venda, WhatsApp, download, etc.) quando o evento já existir no GA4.
- Comparar tráfego vs. conversão antes/depois de uma alteração de SEO — para distinguir ganho de tráfego de ganho real de negócio.

## Regras que continuam valendo com ou sem integração

- SEO não termina no ranking — toda recomendação considera o KPI real da página (ver `medicao-ciclo.md`), nunca só métricas de tráfego.
- Página que ganha tráfego e perde conversão é regressão, não sucesso — sinalize isso explicitamente se os dados mostrarem esse padrão.
- Sem dado real de conversão (via integração ou fornecido pelo usuário), marque a linha de "Conversão" do checklist final como "não avaliada", nunca como aprovada por suposição.
