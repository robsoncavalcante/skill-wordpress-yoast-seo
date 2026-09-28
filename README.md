# SKILL Wordpress SEO - Yoast - SEO

Skill aberta para Claude focada em estratégia, criação, auditoria e otimização de SEO em sites WordPress, com suporte prático ao Yoast SEO Premium.

A Skill foi desenhada para não transformar SEO em uma lista de bolinhas verdes. Ela prioriza intenção de busca, qualidade do conteúdo, arquitetura, experiência, evidência, requisitos técnicos e objetivo de negócio. O Yoast entra como camada de diagnóstico e validação.

> Versão atual: **v1.0-rc1**

## O que esta Skill faz

- cria conteúdos novos a partir de contexto, intenção e pesquisa;
- audita e otimiza conteúdos já existentes;
- trata páginas publicadas de forma conservadora antes de alterar URL, slug, H1, canonical ou intenção;
- pesquisa SERP e compara páginas concorrentes sem copiar conteúdo;
- executa Gap Analysis;
- seleciona frase-chave principal, sinônimos e frases relacionadas;
- verifica canibalização e mapeamento Keyword × URL;
- organiza topic clusters e linking interno;
- orienta SEO Title, meta description, slug e social metadata;
- configura e interpreta Yoast SEO Premium;
- avalia Schema, robots, canonical, sitemap e indexabilidade;
- cobre artigos, páginas institucionais, serviços, landing pages, produtos, categorias e páginas locais;
- trabalha E-E-A-T e YMYL sem transformar esses conceitos em uma pontuação artificial;
- diferencia evidência factual, inferência e hipótese;
- considera imagens, Open Graph, mobile e Core Web Vitals;
- fecha o ciclo com Search Console, GA4, pós-publicação e reotimização;
- registra decisões estratégicas e exceções em Decision Log;
- evita overoptimization e não exige 100% dos indicadores verdes do Yoast.

## Princípio central

```text
INTENÇÃO DE BUSCA
  → QUALIDADE E UTILIDADE DO CONTEÚDO
    → SEO REAL
      → EXPERIÊNCIA DO USUÁRIO
        → FRASE-CHAVE PRINCIPAL
          → COBERTURA SEMÂNTICA
            → FRASES-CHAVE RELACIONADAS
              → RECOMENDAÇÕES DO YOAST
```

**Yoast é validador, não estrategista.**

Uma recomendação do plugin pode terminar como:

- `CORRIGIR`
- `MELHORAR`
- `ACEITAR`
- `IGNORAR COM JUSTIFICATIVA`
- `NÃO APLICÁVEL`

## Instalação no Claude Code pelo GitHub

Este repositório está estruturado como um marketplace compatível com o sistema de plugins/skills do Claude Code.

Adicione o marketplace:

```text
/plugin marketplace add robsoncavalcante/skill-wordpress-yoast-seo
```

Depois instale a Skill:

```text
/plugin install wordpress-seo@skill-wordpress-yoast-seo
```

Após a instalação, inicie uma nova conversa ou recarregue os plugins/skills quando necessário.

### Instalação manual

Também é possível clonar o repositório e copiar a pasta da Skill para o diretório pessoal do Claude Code:

```bash
git clone https://github.com/robsoncavalcante/skill-wordpress-yoast-seo.git
mkdir -p ~/.claude/skills
cp -R skill-wordpress-yoast-seo/skills/wordpress-seo ~/.claude/skills/wordpress-seo
```

Para uso somente em um projeto, copie para:

```text
.claude/skills/wordpress-seo/
```

## Como usar

Depois de instalada, converse normalmente com o Claude. A Skill deve ser ativada quando a solicitação estiver relacionada a SEO em WordPress.

Exemplos:

```text
Quero criar um artigo novo para meu site WordPress sobre [tema].
```

```text
Analise esta URL já publicada e me ajude a otimizar SEO e Yoast sem prejudicar o que já está indexado:
https://exemplo.com/pagina/
```

```text
Compare minha URL com estes concorrentes e faça uma Gap Analysis antes de recomendar alterações.
```

```text
O Yoast está mostrando alerta laranja para o slug. A página já está publicada. Devemos alterar?
```

```text
Analise se existe canibalização entre esta categoria e este artigo.
```

## Fluxo de trabalho

A Skill diferencia duas entradas principais:

### CRIAR

Contexto → intenção → pesquisa → SERP → canibalização → keyword → SEO Brief → estrutura → redação → SEO on-page → Yoast → técnico/Schema → publicação → medição.

### OTIMIZAR

Contexto → status da URL → desempenho existente → intenção → SERP → canibalização → gaps → conteúdo → SEO on-page → Yoast → técnico/Schema → decisão manter/atualizar/expandir/consolidar/redirecionar/remover → medição.

## Estrutura

```text
.claude-plugin/
  marketplace.json
skills/
  wordpress-seo/
    SKILL.md
    references/
      brief-seo.md
      checklist-final.md
      contexto-negocio-site.md
      decision-log.md
      eeat-ymyl-compliance.md
      fluxos-exemplo.md
      fontes-e-evidencias.md
      imagens-social.md
      integrations/
        ga4.md
        search-console.md
        wpwriter.md
      keywords-intencao-canibalizacao.md
      links-clusters.md
      mapa-keywords-urls.md
      medicao-ciclo.md
      performance-mobile.md
      pesquisa-serp-concorrentes.md
      produtos-categorias-local.md
      schema-tecnico-indexacao.md
      wordpress-elementor.md
      workflow-criar.md
      workflow-otimizar.md
      yoast-premium.md
```

## WordPress e plugins

A Skill não assume que todo WordPress usa o mesmo stack. Ela pode adaptar recomendações para cenários com:

- WordPress;
- Yoast SEO / Yoast SEO Premium;
- Elementor / Elementor Pro;
- JetEngine e ecossistema JetPlugins;
- WooCommerce;
- temas e plugins que também geram Schema, canonical, breadcrumbs, Open Graph ou robots.

O objetivo é identificar a fonte de verdade antes de adicionar configurações duplicadas ou conflitantes.

## SERP e concorrentes

Concorrentes são usados para análise competitiva, não como fonte factual automática.

A Skill considera que:

```text
correlação observada na SERP ≠ causalidade comprovada
```

O fato de páginas bem posicionadas terem determinada quantidade de palavras, H2, imagens, FAQs ou tabelas não prova que essas características causaram o ranking.

## YMYL e compliance

Para temas sensíveis ou regulados, a Skill aumenta o nível de rigor das fontes e pode acionar uma camada complementar de compliance.

Este projeto foi pensado para funcionar em conjunto, quando disponível, com:

[publicidade-legal-br](https://github.com/robsoncavalcante/publicidade-legal-br)

A integração é modular. A lógica regulatória não é duplicada dentro desta Skill.

## Integrações opcionais

A pasta `references/integrations/` documenta possibilidades de integração com:

- WordPress/WPWriter;
- Google Search Console;
- Google Analytics 4.

Essas integrações são opcionais. A Skill continua funcionando sem elas e não deve inventar ferramentas, endpoints ou métricas quando não estiverem disponíveis.

## Limitações

- Dados de volume, dificuldade, CPC ou tendência só devem ser usados quando vierem de uma fonte real disponível.
- A Skill não inventa métricas de keyword.
- Core Web Vitals não medidos devem ser marcados como `NÃO AVALIADO`.
- Solicitar indexação no Search Console não garante indexação nem ranking.
- Schema não garante rich results.
- SEO para IA/GEO não garante citação em AI Overviews, ChatGPT, Gemini ou outros sistemas.
- O Decision Log e o Mapa Keyword × URL precisam de uma camada de persistência externa caso você queira mantê-los entre sessões.

## Status do projeto

**v1.0-rc1** é uma release candidate. A arquitetura passou por testes de comportamento simulados e está em fase de validação com casos reais antes de ser marcada como v1.0 definitiva.

## Contribuições

Issues, sugestões e Pull Requests são bem-vindos. Ao propor mudanças, preserve os princípios centrais da Skill:

1. intenção antes do plugin;
2. evidência antes de afirmação;
3. não copiar concorrentes;
4. não inventar métricas;
5. não perseguir bolinhas verdes por princípio;
6. evitar overoptimization;
7. manter regras versionáveis e integrações fora do núcleo sempre que possível.

## Marcas e independência

WordPress, Yoast, Google, Elementor, WooCommerce e demais marcas citadas pertencem aos seus respectivos proprietários. Este projeto é independente e não é afiliado, patrocinado ou endossado por essas empresas.

## Autor

**Robson Cavalcante**

GitHub: [@robsoncavalcante](https://github.com/robsoncavalcante)
