---
aliases: 
tags: 
date created: Friday, August 23rd 2024, 8:45:57 pm
date modified: Friday, August 23rd 2024, 11:55:19 pm
---
Geralmente é muito se debatido quando ou não usar, todavia o certo não seria colocar uma regra generalizada, mas sim analisar cada situação e saber quando usar no memento correto.

Ele é uma alternativa ao git merge.

Quando executamos o rebase, refazemos o historico de commits da branch a partir de outra, é por isso que o rebase é algo muito perigoso. Isso é perigoso pois no processo de rescrita de commits ele altera os hashes, o que torna o tracking mais dificil.

O rebase é muito bom, pois como ele reescreve a estrutura e o historico de commits, ele permite que em vez de situacoes como a de merge commit onde poluem todo o historico de uma branch do git a gente possa ter uma branch mais limpa sem poluir o historico de commits com merge commit messages.

PS: O rebase é baseado na direcao do rebease, no sentido de que sempre deve set considerado de onde e pra onde vai o rebase.

---

Quando não executar o rebase:
- Nunca execute rebase se sua equipe ja tem o mesmo commit que voce caso voce tenha empurrado ja remotamente, com excecao de caso voce tenha empurrado remotamente mas ninguem ainda tenha baixado localmente na maquina deles.
- Nao faca rebase na branch main, faca na branch sua de desenvolvimento

---

Contras de usar rebase:

- Temos um historico de commits muito mais organizado, limpo e menos poluido sem a presenca de commit merge
- Temos um historico linear em producao

---

Pros de usar rebase: