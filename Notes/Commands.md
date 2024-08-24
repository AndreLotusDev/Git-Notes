---
aliases: 
tags: 
date created: Tuesday, August 6th 2024, 11:08:48 am
date modified: Saturday, August 24th 2024, 1:51:50 am
---
git branch - lista todas as branches.

git branch <branch_name> - cria uma branch com o nome especificado .

git branch -d <branch_name> - deleta uma branch, todavia para se fazer isso você não pode estar na branch especificada.

git branch -m <new_branch_name> - renomeia a branch para um novo nome
git branch -m <actual_branch_name> <new_branch_name> - necessário para quando você não está na branch exata.

git checkout <branch_name> - navega para uma branch, caso não exista ele cria essa branch a 
priori, também pode restaurar arquivos.

git switch <branch_name> - faz o mesmo que o git checkout em termos de navegação de branches, todavia por set um commando mais moderno veio com o intuito de fazer somente uma coisa em contraste com o checkout que faz várias coisas.
	git switch - -> volta para a branch anterior que ele estava.

git switch -c <branch_name> - cria uma branch com o nome especificado e depois da switch nela.

git commit -a -m "<commit_message>" - jeito de flow único de commitar já tudo e adicionar uma mensagem.

git diff- analisa os arquivos alterados e mostra a versão previa do HEAD em comparação com a versão atual dos arquivos modificados.

git diff HEAD - mostra a diferença entre todos os arquivos desde o último commit (incluindo arquivos dentro do staging).

git diff --stage/git diff --cached - Ambos os commandos fazem a mesma coisa e mostra a diferença do último commit para com as mudanças que estão em preparação.

git diff HEAD <NOME_DO_ARQUIVO> - Visualiza a diferença do arquivo para o último commit, muito útil para quando seu trabalho na branch e trabalho não commitado tem muitos files, linhas de alteração, ai focamos na diferença de somente um arquivo para não atrapalhar na visualização.

git diff <NOME_DA_BRANCH> <NOME_DA_SEGUNDA_BRANCH> - Compara a diferença entre as branches.
	git diff <NOME_DA_BRANCH> <NOME_DA_SEGUNDA_BRANCH>~1 - Compara as diferenças da branch 1 com a segunda em 1 commit anterior.
	git diff --name-only <NOME_DA_BRANCH> <NOME_DA_SEGUNDA_BRANCH> - Mostra somente a lista de arquivos que são diferentes entre as branches.
	git diff --stat <NOME_DA_BRANCH> <NOME_DA_SEGUNDA_BRANCH> - Mostra somente os status dentro dos arquivos (numeros de linhas modificadas, atualizadas e deletadas).

git diff a1b2c3d e4f5g6h - Compara a diferença entre dois commits.
git diff HEAD HEAD~2 - Compara o estado atual com dois commits anteriores.

git stash | git stash save - Pega todos os arquivos staged e unstaged e movem para o stash.

git stash pop - Remove os items do stash e coloca novamente na branch atual.

git stash apply - Coloca o conteudo do stash dentro da branch atual sem de fato deletar essas coisas do stash, muito útil para quando é necessario aplicar o stash em multiplas branches ao mesmo tempo.

git stash list - Lista todos os stashs que fiz no repositorio e ainda continuam ativos.

git stash apply stash@{2} - Remove o segundo stash da stack.

git stash push -m "Your message" - Cria um stash com uma mensagem customizada em vez da default.

git stash drop stash@{2} - Dropa o stash em especifico da pilha de stashs.

git stash clear - Remove todos os stashs de uma vez só, cuidado pois esse commando não tem desfazer (undo).

git restore - Desfaz as alterações dos arquivos aos quais não estão commitadas, cuidado, pois este commando não tem CTRL Z portando o descarte das alterações são permanentes.

git restore --source HEAD~1 app.js - Restora a versão do arquivo para a versão dettachada do HEAD se for necessário, como por exemplo no HEAD~1 ao qual restora o arquivo app.js para um commit anterior. Você também pode usar o commit hash como ponto de navegação.

git restore --staged <NOME_DO_ARQUIVO> - Move o arquivo do ambiente stage para o ambiente de não comitado. Muito útil para quando você adiciona um arquivo pro stage sem querer, geralmente usamos muito esse commando pela GUI/UI.

git reset <COMMIT> - Ira desfazer o commit, e todos os arquivos tocados por esse commit ficarão em stage para voce modificar ou adicionar em outro commit.

git reset --hard <COMMIT> - Ira desfazer as alterações e descartar os arquivos alterados pelos commits navegados, por exemplo.
	git reset --hard HEAD~2 - Irá desfazer os dois commits, navegar para dois commits atrás e ainda descartar todos os arquivos tocados por esses últimos dois commits.

git remote - Verifica se o projeto local tem link com o remoto.

git remote -v - Verifica e o projeto atual tem link com o remoto e prove as URL's em conjunto.

---

# Github

git clone <URL_DO_PROJETO> - Permite que você clone o projeto, todavia o projeto tem que ter autenticação pro seu usuário ou simplesmente tem que set um projeto do tipo público. 

git remote add <URL> - Adiciona uma nova URL como upstream ou origin se necessário, mas também podemos usar outros nomes se necessário no projeto, todavia isso deve set comunicado a equipe.

git remote rename <ANTIGO> <NOVO> - Renomeia o nome origin e upstream se necessário.

git remote remove <NOME> - Remove o origin/upstream ou qualquer outro criado se necessário.

git push <NOME_REMOTO> <BRANCH> - Empurra as atualizações feitas na branch local para a branch remota.
	git push origin master - Empurra as atualizações que você fez para o origin, e a origin é resolvida na hora de acordo com a URL que você configurar.

git push origin <BRANCH_A>:<BRANCH_B> - Empurra modificações da branch BRANCH_A para a BRANCH_B, é um commando exotico que pode levar a confusão, mas fica de exemplo para caso você precise empurrar coisas de uma branch A para branch B.

git push -u origin main:main - configura que agora as atualizações locais da main vai set empurrada remotamente para a main, e também configura para futuramente qualquer git push efetuado na branch main já seja feito sabendo que é na URL que aponta dentro da origin, não sendo mais necessário efetuar o commando com os flags parametrizadas de forma mais extensa.

git fetch <NOME_DA_BRANCH> - Pega e notifica localmente todas as disparidades e o que falta na branch local para ficar syncada com a branch remota.

git fetch origin - Pega e resolve a URL parametrizada de origin e ve remotamente tudo que ha de disparidade remotamente com suas branches local e notifica para voce o que falta para ambos ambientes ficarem syncados.

git pull - Puxa as diferencas e o que falta para ficar syncado o repositorio local com o remoto, o pull as vezes pode falhar caso as diferencas locais sejam conflitates com as que vem remotamente, exigindo um merge manual do conflito.
	git pull remote <BRANCH_EM_ESPECIFICO> - Puxa as atualizacoes remota de uma branch especifica (nao necessariamente a atual que voce está).

git merge <NOME_DA_BRANCH> - Pega o nome da branch e traz as coisas dela que nao tem na branch atual e joga dentro da branch atual.
	git merge --ff-only feature - Produz um merge sem criar uma mensagem de commit, mas sao poucas as situacoes ao qual isso realmente é possível.
	git merge --no-commit feature - Mesma situacao, todavia ele pausa o processo de commit, e se for necessario criar uma mensagem de commit ele vai te perguntar como voce quer fazer essa mensagem de commit.

git rebase <NOME_DA_BRANCH> - Se voce estiver na branch feature, ele vai analisar o NOME_DA_BRANCH, e reescrever o commit da branch feature no top da NOME_DA_BRANCH e aplicar na branch feature, organizando assim o historico de commits na branch feature.
	git rebase --continue - Necessario quando estamos no fluxo de resolucao de conflitos, excecutamos ele para sinalizar para o git que resolvemos o conflito e que ele pode prosseguir reescrevendo o historico de commits.
	git rebase -i HEAD~4 - Reescreve quatro commits atras de forma iterativa.