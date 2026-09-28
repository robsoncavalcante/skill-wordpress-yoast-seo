# Decision Log — modelo

O Decision Log é a **memória estratégica do projeto**, não só um registro de exceções. Registre:

- **Exceções conscientes** — toda decisão que contraria uma recomendação padrão, do Yoast ou de melhores práticas genéricas, quando a alternativa prejudicaria naturalidade, precisão, UX, intenção, URL consolidada, estratégia, compliance, arquitetura ou conversão.
- **Decisões estratégicas relevantes** — mesmo quando não há exceção a nada, ex.: keyword principal escolhida e por quê, intenção atribuída, URL responsável pela intenção, cluster/pillar a que pertence, se é cornerstone ou não, slug mantido/alterado, canonical, status de indexação, keywords relacionadas aceitas, exceções do Yoast, status de compliance, e a evidência que motivou cada uma dessas escolhas.

Este histórico existe para **impedir que a skill tente "corrigir" depois uma decisão já justificada**, sem evidência nova, e para permitir trabalhar em nível de site/cluster com continuidade entre sessões. Antes de sugerir revisar algo, verifique se já existe uma entrada no log sobre aquele ponto.

**Sobre persistência**: o Decision Log é um formato de registro, não um banco de dados que a skill mantém sozinha. Se a plataforma/sessão não tiver armazenamento persistente entre conversas, diga isso claramente ao usuário — não finja que a skill "lembra" decisões de uma sessão anterior a menos que ele mesmo tenha colado o log existente na conversa atual ou exista um arquivo/projeto externo mantido para isso.

## Formato de cada entrada

```
Data: <data>
URL/página: <url ou "conteúdo novo — <tema>">
Decisão: <o que foi decidido>
Motivo: <por que, em uma frase objetiva>
Evidência considerada: <o que embasou — SERP, dados, arquitetura, compliance, etc.>
Reversível se: <que evidência nova justificaria revisitar isso>
Próxima revisão: <quando reavaliar, se aplicável — ex. "em 4-6 semanas com dado de Search Console">
```

## Exemplo — decisão estratégica (não é exceção, é registro de escolha)

```
Decisão: Keyword principal = "<frase>"; intenção = comercial investigativa.
Motivo: SERP dominada por páginas de comparação/compra, não por conteúdo educativo puro.
Evidência considerada: pesquisa de SERP (Camada 1) + arquitetura do site (esta URL é a única cobrindo a intenção no cluster X).
Cluster/pillar: cluster "<nome>", não é cornerstone.
Reversível se: Search Console mostrar volume relevante vindo de consulta com intenção diferente.
Próxima revisão: em 4-6 semanas, com dado real de Search Console.
```

## Exemplos (formato, não conteúdo a copiar)

```
Decisão: Slug mantido como está.
Motivo: URL já publicada, indexada e com backlinks — mudança exigiria redirect e risco sem ganho claro.
Evidência considerada: URL ranqueando na posição 4 para a keyword principal há 8 meses.
Reversível se: perda sustentada de posição não explicada por outro fator.
```

```
Decisão: Alerta de "frase relacionada com baixa densidade" aceito, campo não ajustado.
Motivo: Forçar mais repetições da frase relacionada prejudicaria a naturalidade do parágrafo.
Evidência considerada: cobertura do subtema já está presente semanticamente sem repetição literal.
Reversível se: dado de Search Console mostrar que a consulta relacionada não está gerando impressão nenhuma.
```

```
Decisão: Canonical deixada automática.
Motivo: Não há razão para canonical manual — página é única, sem duplicidade de parâmetros.
Evidência considerada: nenhuma URL alternativa concorrendo pelo mesmo conteúdo.
Reversível se: surgir uma URL duplicada (ex.: versão com parâmetro de filtro) apontando para o mesmo conteúdo.
```

```
Decisão: Página classificada como cluster, não cornerstone.
Motivo: Cobre um subtema específico, não é hub do tema mais amplo.
Evidência considerada: página pilar já existe e cobre a visão geral, esta página aprofunda um único aspecto.
Reversível se: a página crescer em abrangência a ponto de se tornar referência geral do tema.
```

```
Decisão: noindex global identificado no ambiente.
Motivo: Site em desenvolvimento/staging com "Discourage search engines" ativo em Settings → Reading.
Evidência considerada: página com index=yes no Yoast, mas HTTP header/meta robots do site mostrando noindex.
Reversível se: ambiente migrar para produção — desmarcar antes do lançamento.
```

Mantenha o log como parte da conversa/registro do projeto (não é um arquivo que a skill cria sozinha em disco — é o formato a usar sempre que o usuário pedir para "documentar as decisões" ou quando a skill precisar consultar decisões anteriores dentro da mesma sessão/projeto).
