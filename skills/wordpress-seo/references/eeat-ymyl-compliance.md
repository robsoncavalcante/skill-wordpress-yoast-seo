# E-E-A-T e YMYL/Compliance

## E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness)

Avalie quando relevante, adaptando ao segmento do site:
- Autoria identificada e credenciais compatíveis com o tema.
- Revisão técnica/editorial visível quando aplicável.
- Página "Sobre" completa e verificável.
- Política editorial (como o conteúdo é produzido/revisado).
- Fontes citadas e verificáveis.
- Data de publicação e de atualização visíveis.
- Informações de contato e da empresa completas.
- Transparência geral (quem escreve, quem é dono do site, com que propósito).
- Evidências que sustentam as afirmações feitas (dados, estudos, experiência prática real).

**E-E-A-T não é uma nota.** Não crie nem apresente um "E-E-A-T Score" (ex.: "E-E-A-T = 82/100") — não existe essa métrica proprietária objetiva. A skill analisa sinais qualitativos de experiência, expertise, autoridade e confiança, e comunica achados e lacunas de forma descritiva, nunca como pontuação numérica que sugira precisão que não existe.

## YMYL — quando ativar rigor elevado

Ative automaticamente sempre que o conteúdo envolver: saúde, suplementos, medicamentos, finanças, investimentos, jurídico, crédito, imóveis, profissões regulamentadas, conteúdo voltado a crianças, apostas, ou outros setores regulados.

## Integração modular com `publicidade-legal-br`

Existe uma skill complementar para projetos brasileiros — **publicidade-legal-br** — com arquitetura de compliance publicitário cobrindo CDC, Conar, LGPD, Anvisa, CFM, CFO, CFN, CFP, OAB, CVM e legislação setorial: https://github.com/robsoncavalcante/publicidade-legal-br

**Esta skill nunca copia o conteúdo de `publicidade-legal-br`.** A integração é modular:

1. **Detectar** quando o conteúdo em questão é YMYL/regulado (ver gatilhos acima).
2. **Verificar** se `publicidade-legal-br` está disponível no ambiente do usuário.
3. **Se disponível**, consultar a camada adequada dessa skill antes de redigir.
4. **Se não estiver disponível** e houver acesso web, consultar fontes regulatórias atuais quando necessário (ver `fontes-e-evidencias.md`) — sem inventar o que a skill de compliance diria.
5. **Pedir ao usuário** somente as informações específicas que não puderem ser obtidas de outra forma (não redundar com `contexto-negocio-site.md`).
6. **Aplicar** as restrições de compliance **antes** da redação (briefing de o que pode/não pode ser afirmado).
7. **Revisar novamente** depois da redação, checando se alguma otimização de SEO introduziu alegação problemática.
8. **Revisar também** SEO Title, meta description, CTA, FAQ, Schema e campos sociais quando contiverem alegações sensíveis — não apenas o corpo do texto. Uma alegação problemática no title ou no Schema é tão grave quanto no parágrafo.

**Princípio inegociável: SEO nunca sobrescreve compliance.** Não adicione "cura", "garante", promessa terapêutica ou qualquer alegação não autorizada só porque parece uma keyword forte.

### Caso especial — suplementos no Brasil
- Diferencie suplemento de medicamento na linguagem usada.
- Verifique toda alegação de benefício contra o que é permitido para a categoria.
- Evite promessas terapêuticas.
- Priorize Anvisa e fontes oficiais como referência.
- Sinalize explicitamente ao usuário afirmações que exigiriam comprovação (estudo, registro, laudo) que a skill não pode assumir que existe.
- **Nunca invente comprovação.** Se a informação de sustentação não foi fornecida, diga isso e não redija a alegação como se fosse fato.

Se `publicidade-legal-br` não estiver disponível no ambiente, aplique este módulo com o mesmo rigor de forma independente e avise o usuário que uma checagem jurídica/regulatória formal continua recomendada para publicação final.
