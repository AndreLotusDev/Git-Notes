---
aliases: 
tags: 
date created: Friday, August 16th 2024, 12:34:28 am
date modified: Friday, August 16th 2024, 12:47:28 am
---
Se eu estou trabalhando em um branch e eu tenho trabalho não commitado, quando eu mudo para outra branch eu tenho duas opções:

1 - Ou eu movo os arquivos junto comigo para a branch desejada

2 - Voce nao consegue mudar para a branch, pois há conflitos que precisam set resolvidos e portanto set executado um merge commit

---

PS: Voce pode simplesmente commitar teu trabalho antes de mudar de uma branch para outra, mas isso implica que você terminou a tarefa, ou terminou parte da tarefa, se você está no meio do caminho e não faz muito sentido commitar, não commite, stashar vai set sua melhor opção.

Quando executamos o commando git stash, estamos quando o versionamento dos arquivos, a mudança dele baseado em X branch em um stash, ai tudo que está em stage, unstaged vai para esse ambiente de stage.

Existe um alias, quando digitamos git stash, na verdade estamos executando git stash save.

O commando git stash pop remove as coisas do stash e bota novamente para a branch.