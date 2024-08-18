---
aliases: 
tags: 
date created: Tuesday, August 6th 2024, 11:05:49 am
date modified: Saturday, August 17th 2024, 11:02:57 pm
---
O git head é uma estrutura de controle de versionamento dentro do GIT, quando commitamos uma coisa, cada commit tem um HEAD gerado por HASH ao qual é único, isso permite que possamos navegar entre os milhares de commit com facilidade e permite que cada commit tenha seu HASH único.

Os HEAD são separados em dois modos, os HEAD que são o último COMMIT da BRANCH e os HEAD que são relacionados ao commit que não são o último e mais recente da branch (dettached).

Quando estamos no modo dettached, significa que não estamos no último commit daquela branch, ou seja, estamos viajando no tempo em um commit anterior, com isso sobra para nós 3 opções:
	1 - Eu posso ficar na branch dettached e observar o histórico, ver como o projeto era numa versão especifica e coletar informações.
	2 - Posso voltar para o head, ou seja, voltar para o commit mais recente.
	3 - A partir dessa branch no commit dettached é possível criar uma branch e fazer alterações a partir dela.

Quando usamos o git checkout automaticamente nos movemos para um commit em especifico e dettachamos a posição do head para o commit em especifico, isso significa que não estamos em uma branch em especifico, mas sim em um commit e só.