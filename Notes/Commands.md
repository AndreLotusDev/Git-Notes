---
aliases: 
tags: 
date created: Tuesday, August 6th 2024, 11:08:48 am
date modified: Sunday, August 18th 2024, 10:23:52 pm
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

git diff- analisa os arquivos alterados e mostra a versão previa do HEAD em comparação com a versão atual dos arquivos modificados.

git diff HEAD - mostra a diferença entre todos os arquivos desde o último commit (incluindo arquivos dentro do staging)

git diff --stage/git diff --cached - Ambos os commandos fazem a mesma coisa e mostra a diferença do último commit para com as mudanças que estão em preparação.

git diff HEAD <NOME_DO_ARQUIVO> - Visualiza a diferença do arquivo para o último commit, muito útil para quando seu trabalho na branch e trabalho não commitado tem muitos files, linhas de alteração, ai focamos na diferença de somente um arquivo para não atrapalhar na visualização.

git diff <NOME_DA_BRANCH> <NOME_DA_SEGUNDA_BRANCH> - Compara a diferença entre as branches.
	git diff <NOME_DA_BRANCH> <NOME_DA_SEGUNDA_BRANCH>~1 - Compara as diferenças da branch 1 com a segunda em 1 commit anterior
	git diff --name-only <NOME_DA_BRANCH> <NOME_DA_SEGUNDA_BRANCH> - Mostra somente a lista de arquivos que são diferentes entre as branches
	git diff --stat <NOME_DA_BRANCH> <NOME_DA_SEGUNDA_BRANCH> - Mostra somente os status dentro dos arquivos (numeros de linhas modificadas, atualizadas e deletadas)

git diff a1b2c3d e4f5g6h - Compara a diferença entre dois commits
git diff HEAD HEAD~2 - Compara o estado atual com dois commits anteriores

git stash | git stash save - Pega todos os arquivos staged e unstaged e movem para o stash

git stash pop - Remove os items do stash e coloca novamente na branch atual

git stash apply - Coloca o conteudo do stash dentro da branch atual sem de fato deletar essas coisas do stash, muito útil para quando é necessario aplicar o stash em multiplas branches ao mesmo tempo.

git stash list - Lista todos os stashs que fiz no repositorio e ainda continuam ativos.

git stash apply stash@{2} - Remove o segundo stash da stack

git stash push -m "Your message" - Cria um stash com uma mensagem customizada em vez da default.

git stash drop stash@{2} - Dropa o stash em especifico da pilha de stashs

git stash clear - Remove todos os stashs de uma vez só, cuidado pois esse commando não tem desfazer (undo).

git restore - Desfaz as alterações dos arquivos aos quais não estão commitadas, cuidado, pois este commando não tem CTRL Z portando o descarte das alterações são permanentes.

git restore --source HEAD~1 app.js - Restora a versão do arquivo para a versão dettachada do HEAD se for necessário, como por exemplo no HEAD~1 ao qual restora o arquivo app.js para um commit anterior. Você também pode usar o commit hash como ponto de navegação.

git restore --staged <NOME_DO_ARQUIVO> - Move o arquivo do ambiente stage para o ambiente de não comitado. Muito útil para quando você adiciona um arquivo pro stage sem querer, geralmente usamos muito esse commando pela GUI/UI.

git reset <COMMIT> - Ira desfazer o commit, e todos os arquivos tocados por esse commit ficarão em stage para voce modificar ou adicionar em outro commit.

git reset --hard <COMMIT> - Ira desfazer as alterações e descartar os arquivos alterados pelos commits navegados, por exemplo.
	git reset --hard HEAD~2 - Irá desfazer os dois commits, navegar para dois commits atrás e ainda descartar todos os arquivos tocados por esses últimos dois commits.