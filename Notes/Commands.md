---
aliases: 
tags: 
date created: Tuesday, August 6th 2024, 11:08:48 am
date modified: Tuesday, August 6th 2024, 11:49:16 am
---
git branch - lista todas as branches

git branch <branch_name> - cria uma branch com o nome especificado 

git branch -d <branch_name> - deleta uma branch, todavia para se fazer isso você não pode estar na branch especificada

git branch -m <new_branch_name> - renomeia a branch para um novo nome
git branch -m <actual_branch_name> <new_branch_name> - necessário para quando você não está na branch exata

git checkout <branch_name> - navega para uma branch, caso não exista ele cria essa branch a 
priori, também pode restaurar arquivos

git switch <branch_name> - faz o mesmo que o git checkout em termos de navegação de branches, todavia por set um commando mais moderno veio com o intuito de fazer somente uma coisa em contraste com o checkout que faz várias coisas

git switch -c <branch_name> - cria uma branch com o nome especificado e depois da switch nela

git commit -a -m "<commit_message>" - jeito de flow único de commitar já tudo e adicionar uma mensagem
