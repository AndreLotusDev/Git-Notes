---
aliases: 
tags: 
date created: Friday, August 23rd 2024, 1:23:01 am
date modified: Friday, August 23rd 2024, 3:42:00 pm
---
Em vez de trabalhar diretamente na branch main/master, criamos branches separadas chamada features, desenvolvemos o que precisa set feito e logo apos jogamos novamente para a main, ou dev caso seu projeto tenha camadas de desenvolvimento.

- Trate a main como a branch official e historica do teu projeto
- Multiplos colaboradores podem trabalhar na mesma branch, desde que não seja na main e master, e quando finalizado podem mandar novamente para a master.
- Master e main não deve conter codigo quebrado, digo na maior parte do tempo, o codigo quebrado pode acontecer por meio de bugs imprevistos, mas todo codigo que vai para a main em teoria deveria set minimamente testado.

Geralmente, usamos a branch de feature ate a feature set finalizada, quando ela é finalizada mandamos para dev, stg ou master main como PR, e para isso existem mecanismos de protecao da branch para que se evite de codigo bugado, mal escrito entre de forma indesejada nas branches.

---

Geralmente usamos nomenclaturas como: feat, fix, chore e etc, para sinalizar o que cada feature esta fazendo quando entrar novamente para a main/master.
	Por exemplo, codigos do tipo fix voltarao para a main para corrigr problemas que estao acontecendo em producao.