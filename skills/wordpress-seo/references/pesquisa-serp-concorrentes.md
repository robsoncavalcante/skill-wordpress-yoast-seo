# Pesquisa de SERP e análise de concorrentes

## Pesquisa de SERP (antes de fechar a estratégia de keywords)

Quando houver acesso web, antes de definir frase-chave principal:
- Pesquise a SERP atual para o tema/keyword candidata.
- Identifique a intenção dominante nos resultados (informacional/comercial/transacional/navegacional/local/híbrida).
- Observe o formato predominante (artigo longo, lista, vídeo, produto, ferramenta, comparativo).
- Colete perguntas relacionadas (People Also Ask) quando disponíveis.
- Identifique entidades e subtemas recorrentes entre os top resultados.
- Avalie se há intenções secundárias que merecem página própria ou se cabem na mesma URL.

**Nunca invente volume de busca, CPC, dificuldade de keyword ou qualquer métrica não observada.** Se não houver dado quantitativo disponível, diga isso explicitamente e trabalhe com evidência qualitativa (o que a SERP demonstra, não o que uma ferramenta diria).

## Análise de URL concorrente

Concorrentes podem ser fornecidos pelo usuário para análise. **Nunca copie texto, estrutura autoral específica ou conteúdo protegido.** Decomponha estrategicamente:

- Intenção atendida
- Cobertura temática e profundidade
- Estrutura H1/H2/H3
- Entidades e conceitos cobertos
- Perguntas respondidas
- Fontes citadas
- Links internos/externos usados
- UX editorial (como o conteúdo é apresentado, não só o texto)
- CTA
- Mídia (imagens, vídeo, tabelas)
- Sinais de confiança (autoria, dados, credenciais)
- Title e meta description praticados
- Schema detectável (ver código-fonte/JSON-LD se acessível)
- Diferenciais claros
- Lacunas evidentes

**Concorrente comercial ≠ concorrente orgânico.** Quem disputa o cliente não é necessariamente quem disputa a SERP — analise ambos separadamente quando relevante.

## Concorrente é descoberta competitiva, não fonte factual

Uma página concorrente é excelente para descobrir subtópicos, estrutura, intenção, cobertura, UX, perguntas, posicionamento e lacunas. **Isso não a transforma em fonte factual confiável.** Especialmente em temas YMYL:

```
concorrente          → descoberta competitiva
fonte oficial/científica/regulatória → validação factual
```

Se um concorrente afirma que determinado produto/ingrediente/prática produz determinado efeito, **não assuma que a alegação é verdadeira só porque está bem posicionada**. Verifique em fonte apropriada (ver `fontes-e-evidencias.md`) antes de incorporar a afirmação ao conteúdo — inclusive quando a intenção é apenas "cobrir o que a concorrência cobre".

## Correlação não é causalidade na SERP

O fato de páginas bem posicionadas compartilharem uma característica **não prova** que essa característica causou o ranqueamento. Exemplos de correlações que não devem virar regra: número de palavras, quantidade de H2, presença de FAQ, presença de tabelas, número de imagens, tamanho do conteúdo.

Não conclua "os primeiros resultados têm 2.500 palavras, então precisamos de 2.500 palavras". Analise intenção, utilidade, autoridade, backlinks, força de marca, qualidade do conteúdo, experiência (E-E-A-T) e demais sinais quando disponíveis. A SERP é evidência competitiva — o que os concorrentes fazem e cobrem — não um experimento causal sobre o que faz alguém ranquear.

## Gap Analysis (Content Gap / SERP Gap)

Monte a matriz:

```
NOSSA PÁGINA  ×  CONCORRENTE A  ×  CONCORRENTE B  ×  SERP
```

E responda:
- O que os concorrentes cobrem que nós não cobrimos?
- O que cobrimos que os concorrentes não cobrem (diferencial a reforçar)?
- O que falta em ambos, mas a SERP (PAA, subtemas recorrentes) demonstra que o usuário procura?
- Como produzir algo mais original, útil, confiável e completo — não apenas "mais longo"?

## People Also Ask / perguntas relacionadas — e FAQ Schema

Quando disponíveis, decida por pergunta, **nesta ordem, sem pular etapas**:

1. Esta pergunta é útil para o usuário desta página específica?
2. Ela pertence ao escopo desta página, ou é outra intenção (candidata a página própria)?
3. Deve ser respondida no corpo do texto, em uma seção de FAQ, ou em outro conteúdo?
4. Schema de FAQ é apropriado para o que foi escrito (a resposta no Schema precisa corresponder ao texto visível)?
5. Existe elegibilidade/benefício atual para este tipo de rich result neste site/mercado? (isso muda com o tempo — não assuma sem checar quando for uma decisão relevante).

**Não crie FAQ artificialmente só para obter o Schema.** Não prometa ao usuário que o FAQ Schema vai gerar rich result — a exibição depende do buscador, não é garantida por adicionar o markup.

## Featured snippets

Identifique oportunidades reais: definições diretas, listas numeradas, passo a passo, tabelas comparativas, respostas curtas e diretas logo após um H2/H3 relevante. Não deforme o artigo inteiro tentando forçar um snippet — a resposta direta deve ser um trecho natural do conteúdo, não um apêndice manipulado. Da mesma forma, não prometa ao usuário que a página vai obter o featured snippet — trate como oportunidade estrutural, não como resultado garantido.
