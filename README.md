# Mundo RD Station 2026 — Hub editorial

Hotsite oficial de cobertura do **Mundo RD Station 2026**, evento exclusivo da RD Station para ~500 clientes e parceiros, de 3 a 5 de agosto de 2026 no Costão do Santinho Resort, em Florianópolis.

Site oficial do evento: [mundo.rdstation.com](https://mundo.rdstation.com/)
Hub online: [rd-eduardo-campos.github.io/mundo-rd](https://rd-eduardo-campos.github.io/mundo-rd/)

## O que este repositório serve

Quatro superfícies pensadas para um mesmo conteúdo destilado pelo Cérebro RD a partir do áudio das palestras (Plaud transcreve, Claude estrutura):

1. **Hub editorial (`/`)** — magazine digital com capa, sumário, carômetro das vozes, seções por palco, citação em destaque, últimas reportagens e expediente. Cada palestra vira uma matéria editorial completa.
2. **Tela cinematográfica (`/vozes.html`)** — página fullscreen sem interação, com rotação automática de frases marcantes em tipografia gigante. Pensada para rodar em TVs do Costão durante o evento.
3. **Press kit (`/imprensa.html`)** — boilerplate em três tamanhos copiáveis, big numbers, biblioteca de frases citáveis com atribuição pronta, fotos em alta dos palestrantes para download e contato da assessoria.
4. **Páginas de palco (`/palcos/*.html`)** — índice editorial por palco com listagem das sessões.

## Estrutura

```
.
├── index.html                 ← Home (magazine + carômetro de vozes)
├── vozes.html                 ← Tela cinematográfica para TVs
├── imprensa.html              ← Press kit para imprensa e PR
├── palcos/
│   ├── tendencias.html
│   └── mentoria-aberta.html
├── palestras/
│   ├── martha-gabriel-pensamento-critico.html
│   ├── lideranca-era-ia-bial-laercio-bruno.html
│   └── avelar-maryink-era-das-pessoas.html
├── assets/
│   ├── logo-mundo-rd.png
│   ├── bg-monocromatico-*.png   ← backgrounds monocromáticos
│   ├── bloco-*.png              ← patterns geométricos
│   └── speakers/                ← fotos em alta dos palestrantes
├── llms.txt                   ← sumário do hub para LLMs
├── robots.txt                 ← liberação explícita pra crawlers de IA
├── sitemap.xml                ← mapa de URLs
├── .nojekyll                  ← força GitHub Pages a servir como estático
└── .gitignore
```

## Identidade visual

Paleta Mundo RD Station 2026:

- Petróleo `#022538`
- Cyan `#00C9F2`
- Roxo `#A35CFF`
- Lima `#D7F26B`

Vocabulário geométrico: semicírculos, arcos, círculos concêntricos, triângulos (estilo Bauhaus).

Tipografia: Fraunces (serif display) + Inter (sans UI).

## LLM-ready e SEO

- JSON-LD em todas as páginas (BusinessEvent, Article, Person, CollectionPage, BreadcrumbList, ItemList, WebPage)
- Open Graph + Twitter Card completos
- `canonical`, `keywords`, `theme-color`, `robots` com `max-snippet:-1`
- `llms.txt` na raiz com sumário humano-readable
- `robots.txt` liberando explicitamente GPTBot, ClaudeBot, ChatGPT-User, PerplexityBot, Google-Extended, Applebot-Extended, CCBot e principais crawlers de IA
- `sitemap.xml` com prioridades e changefreq

## Mobile-first e acessibilidade

- Nav mobile como chips scrollable horizontal
- `viewport-fit=cover` para iPhone com notch
- Tipografia responsiva com `clamp()` em todas as headlines
- `focus-visible` com outline cyan, `tap-highlight-color` brand
- `skip-link` "Pular para o conteúdo" em todas as páginas internas
- `<main id="conteudo">` + `<nav aria-label>` + ARIA landmarks
- `prefers-reduced-motion` respeitado

## Como o conteúdo entra

O conteúdo é gerado pelo pipeline do Cérebro RD a partir do áudio capturado na mesa de som. Este repo recebe apenas os HTMLs aprovados. Origem do pipeline e regras de curadoria estão no projeto interno `cerebro-rd-mundo-rd`.

Páginas ficam online em URL direta desde o commit. Indexação no menu acontece depois da aprovação de branding.

## Deploy

GitHub Pages servindo do branch `main`, raiz do repositório.
