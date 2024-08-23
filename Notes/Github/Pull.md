---
aliases: 
tags: 
date created: Monday, August 19th 2024, 1:28:25 am
date modified: Thursday, August 22nd 2024, 11:05:37 pm
---
Basicamente o git pull combina dois commandos, o git fetch e git pull (ele mesmo), ele performa uma operacao de trazer tudo que nao tem localmente de acordo com as informacoes que tem remotamente, isso quando é possivel, digo isso pois há vezes que dependendo do conteudo local pode se produzir conflitos na hora de trazer o conteudo do remoto, exigindo assim que seja feito um merge de conflitos manual localmente que a posteriori deve set empurrado remotamente.

Se voce der o commando git pull sem especificar a branch, o commando sera executado na branch que voce esta atualmente.