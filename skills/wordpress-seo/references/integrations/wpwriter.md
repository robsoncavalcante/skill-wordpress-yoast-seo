# Integração opcional — WPWriter (conceitual)

A skill principal é agnóstica de ferramenta — este arquivo só se aplica quando o usuário tiver um MCP/integração equivalente ao WPWriter disponível na sessão. Se não estiver disponível, todo o workflow continua funcionando manualmente (o usuário aplica as mudanças direto no WordPress/Yoast).

**Marcação**: tudo abaixo é **integração conceitual**. Nenhum nome de tool, endpoint ou schema de chamada é assumido aqui — se um MCP de WordPress estiver de fato conectado na sessão, confirme as tools reais disponíveis (via listagem do próprio ambiente) antes de assumir que uma capacidade existe.

## O que uma integração deste tipo poderia, em conceito, fazer

- **Ler conteúdo** — recuperar o conteúdo publicado de um post/página/produto sem pedir para o usuário colar manualmente.
- **Consultar SEO** — ler o estado atual de campos Yoast (title, meta description, keyword, index/canonical) de uma URL.
- **Atualizar campos** — aplicar as configurações de Yoast decididas no processo (`yoast-premium.md`) diretamente, em vez de instruir o usuário a preencher manualmente.
- **Trabalhar ALT de imagens** — ler e atualizar texto alternativo em lote, seguindo os critérios de `imagens-social.md`.
- **Aplicar alterações de conteúdo** — publicar/atualizar o corpo do post conforme decidido em `workflow-criar.md`/`workflow-otimizar.md`.
- **Validar resultado** — reler o estado após a alteração para confirmar que foi aplicada corretamente (equivalente ao checklist pós-publicação de `medicao-ciclo.md`).

## Como isso se encaixa no fluxo principal

Quando uma integração deste tipo estiver disponível:
1. O SKILL.md e os workflows continuam sendo a fonte da decisão estratégica — a integração só executa o que já foi decidido.
2. Nunca pule etapas de pesquisa/brief/decisão só porque a aplicação técnica ficou mais fácil.
3. Sempre valide o resultado após aplicar (não assuma sucesso silencioso).
4. Se a integração falhar ou não tiver a capacidade esperada, caia de volta ao fluxo manual sem bloquear o usuário.

## Limitação conhecida

Como esta skill precisa funcionar para qualquer projeto WordPress do usuário — inclusive sites sem nenhum MCP conectado — nenhuma etapa do fluxo principal pode depender desta integração para funcionar. Trate-a sempre como acelerador opcional, nunca como pré-requisito.
