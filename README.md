ï»¿# 7 Provas para Qualquer IA

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![7 Provas para Qualquer IA](guia/assets/banner.jpg)](https://inematds.github.io/sete-provas-ia/guia/)

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

## O que êÂ©

SêÂ£o sete pedidos de trabalho prontos para copiar: uma pêÂ¡gina de venda, um painel de vendas, uma apresentaêÂ§êÂ£o, um explicativo animado, um editor de fotos, um jogo 3D e uma central de agentes. Cada pedido vem em trêÂªs formas: para um agente que trabalha numa pasta (Claude Code, Codex, Cursor), para uma janela de chat (Agnes, ChatGPT, Gemini) e como briefing para uma pessoa, sem IA nenhuma. Serve para comparar modelos, escolher ferramenta ou treinar uma equipe. Os dados, o gabarito e o avaliador por script vêÂªm junto; para usar basta copiar o texto, e para o avaliador, ter Python 3.

## ê°Å¸ââ Guia de uso

Guia completo (landing + passo a passo, com botêÂ£o de copiar em cada prompt): **https://inematds.github.io/sete-provas-ia/guia/**

## As 7 provas

| # | Prova | Arquivo entregue | A parte difêÂ­cil |
|---|---|---|---|
| 1 | PêÂ¡gina de venda | `index.html` | um êÂºnico caminho (teste grêÂ¡tis) e uma cena que faz parar de rolar |
| 2 | Painel de vendas | `painel.html` | dados sujos de propêÂ³sito: limpar, mostrar o que consertou, clicar no nêÂºmero |
| 3 | ApresentaêÂ§êÂ£o de vendas | `apresentacao.html` | preêÂ§o que mudou, conta errada e nêÂºmero proibido nas anotaêÂ§êÂµes |
| 4 | Explicativo animado | `explicativo.html` | 20 s sem voz, 1920 x 1080, em loop, para uma crianêÂ§a de 10 anos |
| 5 | Editor de fotos | `editor.html` | 8 ferramentas funcionando de verdade |
| 6 | Jogo de direêÂ§êÂ£o 3D | `jogo.html` | divertido em 10 s, vitêÂ³ria e derrota |
| 7 | Central de agentes | `central.html` | pausar, parar, falha e execuêÂ§êÂµes antigas, com o agente atrêÂ¡s de uma funêÂ§êÂ£o |

## As trêÂªs formas

| Pasta | Para | O que muda |
|---|---|---|
| `prompts/<idioma>/agente/` | Claude Code, Codex, Cursor, Antigravity, Gemini CLI, OpenCode | lêÂª os dados da pasta, grava arquivos e um `ENTREGA.md` |
| `prompts/<idioma>/chat/` | Agnes, ChatGPT, Gemini, Claude.ai, DeepSeek, Grok, Copilot | responde com um êÂºnico HTML; os dados vêÂ£o colados no fim do pedido |
| `prompts/<idioma>/pessoa/` | uma pessoa ou equipe, sem IA | tempo sugerido e como serêÂ¡ avaliado |

Idiomas: `pt`, `en`, `es`. Imagem e vêÂ­deo sêÂ£o opcionais em todas as formas: quem tem gerador (exemplo: Higgsfield, Agnes, Codex) usa; quem nêÂ£o tem desenha em cêÂ³digo.

**Precisa de:** Python 3 (sem bibliotecas extras) e, de preferêÂªncia, Chrome ou Chromium, que o avaliador usa para abrir a pêÂ¡gina escondido e ler os nêÂºmeros calculados pelo JavaScript; sem ele, esses nêÂºmeros viram AVISO. No Windows, troque `python3` por `py`. Sem git: botêÂ£o "Code ê¢â¬Âº Download ZIP". A **semente** êÂ© um nêÂºmero fixo que faz os dados saêÂ­rem sempre iguais, por isso o gabarito nunca muda.

## O processo, do inêÂ­cio ao fim

| # | Passo | Comando | Quem faz |
|---|---|---|---|
| 1 | Gerar os dados e o gabarito (jêÂ¡ vêÂªm prontos; sêÂ³ se mudar a semente) | `python3 kit/gerar_dados.py` | ê¢Å¡â¢ê¯Â¸Â script |
| 2 | Montar os 21 prompts de cada idioma a partir de `kit/provas/<idioma>.json` e atualizar o guia | `python3 kit/montar.py` | ê¢Å¡â¢ê¯Â¸Â script |
| 3 | Escolher prova, forma e concorrentes | ê¢â¬â | ê°Å¸Â§Â  vocêÂª |
| 4 | Preparar uma pasta por concorrente (prompt + dados) | `python3 kit/preparar.py 2 corrida/claude/02` | ê¢Å¡â¢ê¯Â¸Â script |
| 5 | Rodar: colar o `PROMPT.md` no agente, no chat ou entregar êÂ  pessoa | ê¢â¬â | ê°Å¸Â¤â IA ou ê°Å¸Â§â pessoa |
| 6 | Conferir o que dêÂ¡ para medir sem IA | `python3 kit/avaliar.py 2 corrida/claude/02` (`--chat` para entrega de chat) | ê¢Å¡â¢ê¯Â¸Â script |
| 7 | Abrir a entrega, usar 5 min e preencher a ficha de 10 pontos | `avaliar/ficha.md` | ê°Å¸Â§Â  vocêÂª |
| 8 | Comparar as fichas e anotar tempo e custo de cada concorrente | ê¢â¬â | ê°Å¸Â§Â  vocêÂª |

ConferêÂªncias do prêÂ³prio kit: `python3 kit/gerar_dados.py --conferir` (dados batem com a semente) e `python3 kit/montar.py --conferir` (prompts e guias atualizados).

## Gabarito (sem IA)

- **Prova 2:** `vendas.csv` tem 1.470 linhas e cinco problemas plantados. Limpo: 1.430 pedidos, R$ 50.162,10. VersêÂ£o de chat (`vendas-mini.csv`): 224 pedidos, R$ 7.831,00. Limpeza de referêÂªncia: `python3 kit/limpar.py dados/vendas.csv`.
- **Prova 3:** preêÂ§o certo R$ 89/kg (nêÂ£o 95), soma certa 157 pessoas (nêÂ£o 140), R$ 130 do concorrente proibido. Tudo em `dados/gabarito.json`.

## Teste real

As provas 2 e 3 na forma chat foram rodadas no Claude Sonnet (assinatura, conversa sem ferramentas). Entregas e capturas em `exemplos/chat-sonnet/`. No Agnes e nos outros chats o formato ainda nêÂ£o foi medido.

## Estrutura

```
prompts/{pt,en,es}/{agente,chat,pessoa}/   21 prompts por idioma (gerados)
kit/provas/{pt,en,es}.json                  fonte êÂºnica dos prompts
kit/gerar_dados.py  kit/limpar.py  kit/avaliar.py  kit/montar.py  kit/preparar.py
dados/  vendas.csv  vendas-mini.csv  notas.txt (+ en/ es/)  gabarito.json
avaliar/ficha.md  ficha.en.md  ficha.es.md   ficha de 10 pontos (PT, EN, ES)
exemplos/chat-sonnet/                       teste real no modo chat
guia/                                       landing + guia PT/EN/ES
```

LicenêÂ§a MIT. Parte do ecossistema [INEMA.CLUB](https://inema.club).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>