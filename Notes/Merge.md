---
aliases: 
tags: 
date created: Tuesday, August 6th 2024, 12:00:58 pm
date modified: Wednesday, August 7th 2024, 12:18:39 am
---

Nós normalmente não commitamos diretamente na main, para isso criamos branches de suporte, como a famosa feature.

Fazemos tudo que é necessário nessa branch e quando finalizamos jogamos novamente para a main, master ou trunk (chame como quiser).

O fluxo para se fazer merge é o seguinte (em duas etapas):

1. Fazer o checkout da branch de suporte
    - git checkout feature/nome-da-branch
    1.1 - faça as alterações necessárias

2. Fazer o merge da branch de suporte para a main
    - git checkout main
    - git merge feature/nome-da-branch

---

