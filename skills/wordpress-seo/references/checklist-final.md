# Checklist final por URL

Ao concluir o trabalho em uma URL (criação ou otimização), gere um painel como o modelo abaixo, adaptado ao que de fato foi avaliado no projeto.

## Estados válidos

| Símbolo | Significado |
|---|---|
| ✓ | OK — checado e correto |
| ⚠ | ATENÇÃO — pendente ou com ressalva |
| ○ | NÃO AVALIADO — não foi possível checar (ex.: sem dado de PageSpeed) |
| — | NÃO APLICÁVEL — não faz sentido para este tipo de página |
| ⏳ | AGUARDANDO DADOS — depende de tempo/dado externo (ex.: Search Console) |

**"Não avaliado" (○) nunca é aprovação.** Não use ✓ quando na verdade não foi checado — isso é o erro mais grave que este painel pode cometer, porque passa confiança falsa ao usuário.

```
SEO estratégico: ✓
Intenção: ✓
Conteúdo: ✓
Keyword principal: ✓
Relacionadas: ✓ / alertas aceitos (ver decision log)
Links internos: ✓
Links externos: ✓
Yoast: ✓ / exceções documentadas
Schema: ✓
Social: ✓
Canonical: ✓
Indexação: ⚠ aguardando produção
Compliance: ✓ / —
Mobile: ○ não avaliado
Performance: ○ não avaliado
Search Console: ⏳ acompanhar
Conversão: ○ não avaliada
```

Regras:
- Cada linha marcada ✓ deve corresponder a algo real que foi checado nesta conversa — não gere o painel só para parecer completo.
- ○ (não avaliado) é uma resposta honesta válida e frequente — melhor do que inventar ou marcar ✓ por suposição.
- Se houver exceções documentadas no decision log, referencie-as na linha correspondente em vez de só marcar ✓ genérico.
- Adapte as linhas ao tipo de página — uma categoria/taxonomia não precisa de linha de "Conversão" da mesma forma que uma landing page (marque — ); um artigo institucional pode não ter "Compliance" aplicável (marque —).
- Yoast 100% verde não é, por si só, motivo para marcar tudo ✓ — cada linha reflete o que foi avaliado naquele domínio específico (intenção, arquitetura, técnico, compliance etc.), não a pontuação do plugin.
