---
aliases: 
tags: 
date created: Tuesday, July 16th 2024, 6:58:55 pm
date modified: Tuesday, July 16th 2024, 7:05:30 pm
---
Quando criamos um projeto com o commando git init, criamos por debaixo dos panos dentro desse diretório uma pasta .git, ela previamente é oculta.

Ela é respon´savel por controlar o versionamento, os metadados e todo controle de fluxo do GIT.

Com ela especificamos que um folder level está sendo gerenciado pelo GIT.

Alias, ela fica previamente oculta, pois com isso se evita de causar errors acidentais dentro de seu repositório git, tendo em vista que ela controla basicamente tudo do GIT. Isso se dá por convenção de sistemas operacionais que arquivos que começam com . devem set ocultos e que não devem set manipulados diretamente pelos usuários finais, pois são arquivos sensiveis e de configuração. 

PS: Alias, nunca crie um repositorio GIT dentro de outro repositorio GIT.