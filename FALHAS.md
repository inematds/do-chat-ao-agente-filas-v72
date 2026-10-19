# Falhas

| data | o que quebrou | menor correção | tipo |
| --- | --- | --- | --- |
| 2026-10-19 | Tradução EN/ES: comandos do bot (`transcrever:`, `explicativo:`) traduzidos dentro de `<code>`, 3 blocos de código ES devolvidos em PT e fase "Textos" virou "Copy" no EN (mensagem dizia "Texts") | Correção no cache `i18n/<lang>.json` + rodar `traduzir.py` de novo | prompt |
| 2026-10-19 | Capa incluiu números legíveis nos cartões | Edição localizada no image_gen removeu os números | prompt |
