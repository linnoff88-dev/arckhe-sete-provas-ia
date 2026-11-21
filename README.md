# 7 Provas para Qualquer IA

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![7 Provas para Qualquer IA](guia/assets/banner.jpg)](https://inematds.github.io/sete-provas-ia/guia/)

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## O que Ã©

SÃ£o sete pedidos de trabalho prontos para copiar: uma pÃ¡gina de venda, um painel de vendas, uma apresentaÃ§Ã£o, um explicativo animado, um editor de fotos, um jogo 3D e uma central de agentes. Cada pedido vem em trÃªs formas: para um agente que trabalha numa pasta (Claude Code, Codex, Cursor), para uma janela de chat (Agnes, ChatGPT, Gemini) e como briefing para uma pessoa, sem IA nenhuma. Serve para comparar modelos, escolher ferramenta ou treinar uma equipe. Os dados, o gabarito e o avaliador por script vÃªm junto; para usar basta copiar o texto, e para o avaliador, ter Python 3.

## ðŸ“– Guia de uso

Guia completo (landing + passo a passo, com botÃ£o de copiar em cada prompt): **https://inematds.github.io/sete-provas-ia/guia/**

## As 7 provas

| # | Prova | Arquivo entregue | A parte difÃ­cil |
|---|---|---|---|
| 1 | PÃ¡gina de venda | `index.html` | um Ãºnico caminho (teste grÃ¡tis) e uma cena que faz parar de rolar |
| 2 | Painel de vendas | `painel.html` | dados sujos de propÃ³sito: limpar, mostrar o que consertou, clicar no nÃºmero |
| 3 | ApresentaÃ§Ã£o de vendas | `apresentacao.html` | preÃ§o que mudou, conta errada e nÃºmero proibido nas anotaÃ§Ãµes |
| 4 | Explicativo animado | `explicativo.html` | 20 s sem voz, 1920 x 1080, em loop, para uma crianÃ§a de 10 anos |
| 5 | Editor de fotos | `editor.html` | 8 ferramentas funcionando de verdade |
| 6 | Jogo de direÃ§Ã£o 3D | `jogo.html` | divertido em 10 s, vitÃ³ria e derrota |
| 7 | Central de agentes | `central.html` | pausar, parar, falha e execuÃ§Ãµes antigas, com o agente atrÃ¡s de uma funÃ§Ã£o |

## As trÃªs formas

| Pasta | Para | O que muda |
|---|---|---|
| `prompts/<idioma>/agente/` | Claude Code, Codex, Cursor, Antigravity, Gemini CLI, OpenCode | lÃª os dados da pasta, grava arquivos e um `ENTREGA.md` |
| `prompts/<idioma>/chat/` | Agnes, ChatGPT, Gemini, Claude.ai, DeepSeek, Grok, Copilot | responde com um Ãºnico HTML; os dados vÃ£o colados no fim do pedido |
| `prompts/<idioma>/pessoa/` | uma pessoa ou equipe, sem IA | tempo sugerido e como serÃ¡ avaliado |

Idiomas: `pt`, `en`, `es`. Imagem e vÃ­deo sÃ£o opcionais em todas as formas: quem tem gerador (exemplo: Higgsfield, Agnes, Codex) usa; quem nÃ£o tem desenha em cÃ³digo.

**Precisa de:** Python 3 (sem bibliotecas extras) e, de preferÃªncia, Chrome ou Chromium, que o avaliador usa para abrir a pÃ¡gina escondido e ler os nÃºmeros calculados pelo JavaScript; sem ele, esses nÃºmeros viram AVISO. No Windows, troque `python3` por `py`. Sem git: botÃ£o "Code â€º Download ZIP". A **semente** Ã© um nÃºmero fixo que faz os dados saÃ­rem sempre iguais, por isso o gabarito nunca muda.

## O processo, do inÃ­cio ao fim

| # | Passo | Comando | Quem faz |
|---|---|---|---|
| 1 | Gerar os dados e o gabarito (jÃ¡ vÃªm prontos; sÃ³ se mudar a semente) | `python3 kit/gerar_dados.py` | âš™ï¸ script |
| 2 | Montar os 21 prompts de cada idioma a partir de `kit/provas/<idioma>.json` e atualizar o guia | `python3 kit/montar.py` | âš™ï¸ script |
| 3 | Escolher prova, forma e concorrentes | â€” | ðŸ§  vocÃª |
| 4 | Preparar uma pasta por concorrente (prompt + dados) | `python3 kit/preparar.py 2 corrida/claude/02` | âš™ï¸ script |
| 5 | Rodar: colar o `PROMPT.md` no agente, no chat ou entregar Ã  pessoa | â€” | ðŸ¤– IA ou ðŸ§‘ pessoa |
| 6 | Conferir o que dÃ¡ para medir sem IA | `python3 kit/avaliar.py 2 corrida/claude/02` (`--chat` para entrega de chat) | âš™ï¸ script |
| 7 | Abrir a entrega, usar 5 min e preencher a ficha de 10 pontos | `avaliar/ficha.md` | ðŸ§  vocÃª |
| 8 | Comparar as fichas e anotar tempo e custo de cada concorrente | â€” | ðŸ§  vocÃª |

ConferÃªncias do prÃ³prio kit: `python3 kit/gerar_dados.py --conferir` (dados batem com a semente) e `python3 kit/montar.py --conferir` (prompts e guias atualizados).

## Gabarito (sem IA)

- **Prova 2:** `vendas.csv` tem 1.470 linhas e cinco problemas plantados. Limpo: 1.430 pedidos, R$ 50.162,10. VersÃ£o de chat (`vendas-mini.csv`): 224 pedidos, R$ 7.831,00. Limpeza de referÃªncia: `python3 kit/limpar.py dados/vendas.csv`.
- **Prova 3:** preÃ§o certo R$ 89/kg (nÃ£o 95), soma certa 157 pessoas (nÃ£o 140), R$ 130 do concorrente proibido. Tudo em `dados/gabarito.json`.

## Teste real

As provas 2 e 3 na forma chat foram rodadas no Claude Sonnet (assinatura, conversa sem ferramentas). Entregas e capturas em `exemplos/chat-sonnet/`. No Agnes e nos outros chats o formato ainda nÃ£o foi medido.

## Estrutura

```
prompts/{pt,en,es}/{agente,chat,pessoa}/   21 prompts por idioma (gerados)
kit/provas/{pt,en,es}.json                  fonte Ãºnica dos prompts
kit/gerar_dados.py  kit/limpar.py  kit/avaliar.py  kit/montar.py  kit/preparar.py
dados/  vendas.csv  vendas-mini.csv  notas.txt (+ en/ es/)  gabarito.json
avaliar/ficha.md  ficha.en.md  ficha.es.md   ficha de 10 pontos (PT, EN, ES)
exemplos/chat-sonnet/                       teste real no modo chat
guia/                                       landing + guia PT/EN/ES
```

LicenÃ§a MIT. Parte do ecossistema [INEMA.CLUB](https://inema.club).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>