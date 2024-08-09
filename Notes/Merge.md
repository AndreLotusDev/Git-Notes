---
aliases: 
tags: 
date created: Tuesday, August 6th 2024, 12:00:58 pm
date modified: Friday, August 9th 2024, 5:55:08 pm
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

Performar o merge de branch A a branch B não faz automaticamente A set deletada, preste bem atenção nisso, pois caso contrário você terá um monte de branch sobrando dentro de seu projeto git.

---

Quando executamos um commando merge no git, se for necessário resolver os conflitos para mergear a branch em outra branch, quando for finalizado a resolução de problemas é necessário fazer o commit do merge conflict, esse tipo de commit é o um dos poucos que tem dois parents, a maioria só tem um parent linkado com o commit.
