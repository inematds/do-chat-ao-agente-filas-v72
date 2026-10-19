# Filas: dez tarefas e vá dormir — curso (INEMA Learning v7.2)

Curso completo do **degrau 3** da formação [Do chat ao agente](https://inematds.github.io/do-chat-ao-agente-v72/): mandar várias tarefas para uma fila durável, sair de perto e encontrar o trabalho feito, com portão onde precisa de você. A ferramenta é o [inemaccbot](https://inematds.github.io/inemaccbot/guia/) (gateway do Telegram + fila durável).

**Abrir o curso:** https://inematds.github.io/do-chat-ao-agente-filas-v72/

**Other languages:** [English](https://inematds.github.io/do-chat-ao-agente-filas-v72/en/) · [Español](https://inematds.github.io/do-chat-ao-agente-filas-v72/es/)

## As 7 aulas

1. **Do chat à fila** — as quatro garantias de uma fila durável.
2. **O que vai para a fila** — triagem em sozinha, com portão ou fica com você.
3. **A fila caseira em 30 linhas** — `fila-caseira.sh`, interromper e retomar (simulação).
4. **Instalar o inemaccbot** — até o `/ping` responder; pareamento e segredos.
5. **Mandar o lote** — skills, as cinco filas, `/fila`, `/jobs`, código 143.
6. **Portões** — fluxo com portão, `/pronto`, reprovar com correção, `| sombra` (simulação).
7. **O dia seguinte** — conferir, medir as certas na primeira, regra nova e plano com datas.

## Como funciona

| Arquivo | O que é |
|---|---|
| `conteudo/pt/curso.json` | nome, vídeos, página inicial e textos da interface |
| `conteudo/pt/aulas/*.json` | uma aula por arquivo |
| `gerar.py` | monta `index.html` e `aulas/<slug>/index.html` |
| `validar.py` | portão de qualidade (`--links` confere os links externos) |
| `assets/` | CSS, JS, imagens e legendas (`filas.js`/`filas.css`: simulação do portão) |

```bash
python3 gerar.py && python3 validar.py --links
```

EN e ES (`en/`, `es/`): textos em `conteudo/en|es/`, gerados por `traduzir.py` da skill (Codex da assinatura, cache em `i18n/`); capa com texto em `assets/img/capa-en.jpg` e `capa-es.jpg`.

```bash
python3 ~/.claude/skills/formato-curso-v72/scripts/traduzir.py . en es
python3 gerar.py --lang en && python3 gerar.py --lang es
python3 validar.py --lang en && python3 validar.py --lang es
```

HTML estático, sem build e sem backend. O progresso fica só no navegador de quem estuda.

Vídeos da série *Do chat ao agente* ([jornada-agentes](https://github.com/inematds/jornada-agentes), release `video-v2.0.0`). Exercícios originais em [`exercicios/03-filas.md`](https://github.com/inematds/jornada-agentes/blob/main/exercicios/03-filas.md).

Conteúdo aberto e gratuito · [INEMA.CLUB](https://inema.club)

## Mais no INEMA.CLUB

- [Ficha completa deste curso](https://www.inema.club/cursos/326-do-chat-ao-agente-degrau-3-filas-dez-tarefas-e-va-dormir-inemaccbot/)
- [Guia: como aprender inteligência artificial](https://www.inema.club/aprender-inteligencia-artificial/)
- [Todos os cursos](https://www.inema.club/cursos/)
