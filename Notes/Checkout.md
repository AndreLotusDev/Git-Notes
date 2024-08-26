---
aliases: 
tags: 
date created: Tuesday, August 6th 2024, 11:28:33 am
date modified: Monday, August 26th 2024, 8:08:43 pm
---
O git checkout quando é realizado e você tem trabalho dentro da branch que está unstaged você tem algumas opções:

1 - deletar os arquivos e mudar de branch
2 - commitar os arquivos unstaged para a branch antes de sair dela
3 - dar stash nos arquivos da branch, se mudar da branch e recuperar esses arquivos.

A priori por muitas pessoas usarem UI não veem esse processo acontecendo, todavia muitas das vezes o que acontece é o uso da terceira opção.

---

É possível dar checkout baseado em tempo, muito util para quando voce nao lembra exatamente quando e pra onde vc precisa navegar.

- git checkout bugfix@{2.days.ago}