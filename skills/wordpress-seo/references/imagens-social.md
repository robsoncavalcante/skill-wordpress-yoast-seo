# Imagens e Social/Open Graph

## Imagens

Avalie:
- **Filename** — descritivo, sem espaços/caracteres especiais, alinhado ao conteúdo da imagem.
- **ALT** — deve descrever a imagem para quem não pode vê-la. **Não é depósito de keyword.** Se a imagem é puramente decorativa, ALT vazio é aceitável.
- **Contexto** — a imagem reforça o conteúdo ao redor ou é genérica de banco de imagens sem relação real?
- **Legenda** — só quando agrega informação que o ALT não cobre.
- **Compressão e dimensões** — peso adequado ao uso real (thumbnail vs imagem de destaque vs galeria).
- **Formato** — preferir WebP/AVIF quando o ambiente suportar, com fallback.
- **Imagem destacada** — presente e coerente com o conteúdo (é o que normalmente alimenta o Open Graph por padrão).
- **Lazy loading** — apropriado para imagens abaixo da dobra; evitar em imagens críticas para LCP (ver `performance-mobile.md`).

## Social / Open Graph

Avalie:
- Imagem — dimensão correta para o preview de cada rede, sem informação crítica cortada.
- Título e descrição sociais — pensados para gerar interesse no feed, não apenas replicados do SEO Title/meta description.
- Recorte da imagem em diferentes proporções (feed vs card vs story, quando relevante).
- Informação visível antes de possível truncamento do texto.

**Não replique automaticamente SEO Title e meta description para os campos sociais** — são públicos e contextos diferentes (SERP vs feed).

Campos específicos de X/Twitter só precisam ser preenchidos separadamente quando houver razão real para diferenciar da configuração social geral (Open Graph) — caso contrário, deixe herdar.
