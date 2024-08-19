---
aliases: 
tags: 
date created: Sunday, August 18th 2024, 9:50:56 pm
date modified: Sunday, August 18th 2024, 10:04:38 pm
---
O git restore foi criado com o intuito de substituir e diminuir o peso em confusão com o tanto de possibilidade que temos ao usar o git checkout.

PS: o commando git restore desfaz as alterações não commitadas dos arquivos, e tome cuidado, pois não tem CTRL Z para reverter esse commando.

Não é só possível executar o descarte de arquivos como é possível restorar os arquivos para versões anteriores, como por exemplo com o commando: git restore --source HEAD~1 app.js, ao qual o arquivo app.js é nevegado para uma versão atrás da HEAD.

---

O commando restore pode causar certa confusão pelo nome, mas ele também pode mover arquivos do staged para o ambiente de uncommitted, para isso basta caso você tenha adicionado um arquivo ao ambiente de stage executar o seguinte commando:

git restore --staged <NOME_DO_ARQUIVO>