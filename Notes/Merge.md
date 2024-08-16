---
aliases: 
tags: 
date created: Tuesday, August 6th 2024, 12:00:58 pm
date modified: Friday, August 9th 2024, 6:21:57 pm
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

---

Geralmente um conflito de merge é causado quando duas pessoas mexem no mesmo memento no mesmo arquivo e na mesmas linhas, quando isso acontece o git meio que se perde e precisará de ajuda manual de como resolver o conflito de diferença entre as duas branches, para isso ele irá sinalizar quais arquivos estão conflitantes e quais são as linhas que precisam de resolução manual do programador, sendo assim o programador se dispõe manualmente de ajustar e mergear a diferença entre as duas branches.

É aconselhável sempre os dois programadores referente as duas alterações trabalharem em conjunto para acharem uma solução viavel de como incluir as duas adições/atualização/remoção ao mesmo tempo.

PS: Geralmente o merge conflict é feito pelo git, mas dado a natureza de algumas soluções serem mais complexas é altamente recomendado que a pessoa use uma GUI para isso, a maioria da GUI e IDE's fornecem suporte para resolução de conflitos, fazendo o processo set muito menos doloroso, como por exemplo o próprio VS CODE, 'IDE' Open Source.
