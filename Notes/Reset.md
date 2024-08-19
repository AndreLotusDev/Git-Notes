---
aliases: 
tags: 
date created: Sunday, August 18th 2024, 10:17:50 pm
date modified: Sunday, August 18th 2024, 10:20:13 pm
---
Quando executamos o commando git reset, dizemos para o git que fizemos alterações indesejaveis e que queremos desfazer esse commit/commits, seja lá qual seja a motivação por de trás disso.

Podemos executar o commando de duas formas:

git reset <COMMIT> - Ira desfazer o commit, e todos os arquivos tocados por esse commit ficarão em stage para voce modificar ou adicionar em outro commit.

git reset --hard <COMMIT> - Ira desfazer as alterações e descartar os arquivos alterados pelos commits navegados, por exemplo.
	git reset --hard HEAD~2 - Irá desfazer os dois commits, navegar para dois commits atrás e ainda descartar todos os arquivos tocados por esses últimos dois commits.