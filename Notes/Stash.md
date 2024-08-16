---
aliases: 
tags: 
date created: Friday, August 16th 2024, 12:34:28 am
date modified: Friday, August 16th 2024, 1:09:36 am
---
Se eu estou trabalhando em um branch e eu tenho trabalho não commitado, quando eu mudo para outra branch eu tenho duas opções:

1 - Ou eu movo os arquivos junto comigo para a branch desejada

2 - Voce nao consegue mudar para a branch, pois há conflitos que precisam set resolvidos e portanto set executado um merge commit

---

PS: Voce pode simplesmente commitar teu trabalho antes de mudar de uma branch para outra, mas isso implica que você terminou a tarefa, ou terminou parte da tarefa, se você está no meio do caminho e não faz muito sentido commitar, não commite, stashar vai set sua melhor opção.

Quando executamos o commando git stash, estamos quando o versionamento dos arquivos, a mudança dele baseado em X branch em um stash, ai tudo que está em stage, unstaged vai para esse ambiente de stage.

Existe um alias, quando digitamos git stash, na verdade estamos executando git stash save.

O commando git stash pop remove as coisas do stash e bota novamente para a branch.

O Stash por natureza, pode set executado multiplas vezes, quando feito isso ele stacka acumulando uma lista de stashs, ao qual se você não taggeia tem nomes aleatorios, voce pode nomear else para melhorar a organização, por default, quando você da stash apply ele vai pegar o último stash feito e aplicar na branch, caso você queira um especifico é necessário executar o seguinte commando:
	git stash apply stash@{2} - Remove o segundo stash da stack

Normalmente, usando o GIT pelo BASH é quase anormal usar mais de stash por vez, geralmente acumulamos muito stash quando usamos UI, o que torna tudo mais fácil e mais intuitivo, e por muitas vezes esquecemos de deletar o stash quando aplicado.

Por muitas vezes, acabamos acumulando muitos stash, principalmente quando usamos rotineiramente somente o apply. Portanto é bom verificar periodicamente com o commando git stash list para ver quantos stashs a gente possui.