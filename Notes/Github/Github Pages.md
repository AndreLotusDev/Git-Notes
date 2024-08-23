---
aliases: 
tags: 
date created: Friday, August 23rd 2024, 12:39:15 am
date modified: Friday, August 23rd 2024, 12:58:14 am
---
Permite que o desenvolvedor ao empurrar o codigo para o repositorio remoto do github crie atualizacoes constantes no github em forma de pagina. Muito util para projetos pequenos.

Lembrando que essa funcionalidade funciona somente com páginas do tipo estática. Ou seja, somente JS, HTML e CSS, nada de server side rendering com python, php e c#.

Geralmente essas paginas terminam com github.io, sinalizando que sao hosteadas por github pages.

Existem dois tipos de github pages:
	- User Site, é um site unico ao qual cada usuario de github pode ter somente um, ao qual ele pode hostear informacoes professional dele e etc e geralmente segue o seguinte padrao: username.github.io
	- Project Site, é ilimitado e geralmente são direcionado para os projetos do usuário, geralmente o padrão é username.github.io/repo-name.

Geralmente é muito recomendado se utilizar github page para projetos pequenos, todavia o mesmo não é verdade para projetos grandes e de muito tráfico, pois o tier que hosteamos o github pages é free, e portando provavelmente a máquina virtual ou pod alocado a isso é muito básico e frágil (leia-se pouco resiliente).