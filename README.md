# Mundo RD Station 2026 — Hub de conteúdo

Hotsite de conteúdo do **Mundo RD Station 2026** — o evento exclusivo da RD Station para ~500 clientes e parceiros, de 3 a 5 de agosto de 2026, no Costão do Santinho Resort, em Florianópolis.

Site oficial do evento: [mundo.rdstation.com](https://mundo.rdstation.com/)

## O que é este repositório

Este repo serve, via **GitHub Pages**, o hub de conteúdo pós-palestras: uma página por sessão, organizada por palco, com insights destilados, quotes em destaque e contexto do speaker.

O conteúdo é gerado pelo pipeline do Cérebro RD a partir do áudio capturado na mesa de som durante o evento — transcrição via Plaud e estruturação via Claude. Este repo recebe apenas os HTMLs aprovados.

## Estrutura

```
.
├── index.html                              ← Home do hub
├── palestras/
│   └── martha-gabriel-pensamento-critico.html  ← Uma palestra
└── assets/                                 ← Identidade visual Mundo RD
    ├── logo-mundo-rd.png
    ├── bg-monocromatico-*.png
    └── bloco-*.png
```

## Identidade visual

Paleta Mundo RD Station 2026:

- Petróleo `#022538`
- Cyan `#00C9F2`
- Roxo `#A35CFF`
- Lima `#D7F26B`

Vocabulário geométrico: semicírculos, arcos concêntricos, triângulos e quartos de círculo (estilo Bauhaus).

## Deploy

GitHub Pages servindo da branch `main`, raiz do repositório.
