---
aliases: 
tags: 
date created: Thursday, August 8th 2024, 11:43:18 pm
date modified: Thursday, August 8th 2024, 11:51:52 pm
---
# Exemplo do uso da feature no git flow

Certifique-se de estar na branch develop
	git checkout develop

Puxe as últimas mudanças de develop (opcional, mas recomendado)
	git pull origin develop

Crie a nova branch feature
	git checkout -b feature/nome-da-feature

Pronto, agora voce estara na branch da nova feature, os primeiros passos a posteriori foram par;a certificar que voce tinha a branch develop mais atualizada antes de comecar o desenvolvimento paralelo, é claro que nada te impede de mergear a develop novamente durante o meio do desenvolvimento para ver problemas de merge caso voce se mantenha muito tempo desenvolvendo na mesma branch e a branch pai de referencia (develop) receba muitas atualizacoes.

---

- Faca o desenvolvimento necessario nessa branch
- Adicione todos os commits para stage 
	- git add .

- Faca o commit desses arquivos preparados
	- git commit -m "Descrição das mudanças realizadas na feature"
	- De preferencia com o commit bem descritivo

---

Apos terminar faca o push da branch remotamente ao qual voce estava trabalhando de forma exclusivamente local.
	git push origin feature/nome-da-feature

Isso é importante fazer periodicamente, tanto o push remoto quando commits temporarios e mais atomicos, isso permite que voce volte versoes a posteriori caso nao goste e tambem permite caso o seu pc de alguma falha o servidor remoto tenha o codigo mais atualizado para que voce possa restaurar ele assim que possivel.

---

Faca o merge da feature em dev

Certifique-se de estar na branch develop
	git checkout develop

Puxe as últimas mudanças de develop
	git pull origin develop

Mescle a branch feature na branch develop
	git merge --no-ff feature/nome-da-feature

Isso é possível por merge direto, ou também pode set feito uma abertura de um PR onde outro desenvolvedor irá analisar o PR e somente irá mergear em último caso, caso tudo esteja tudo ok, se tiver algo em não conformidade é necessário fazer alterações pontuais e fazer um novo commit e push para o servidor remoto.

---

Após feito isso é possível fazer a remoção da branch, todavia isso é opcional, tudo vai depender do protocolo da empresa, do protocolo do projeto, do tamanho da equipe, necessidade e outros fatores.

Por questões de limpeza pode se remover a branch ou renomear para _old

Caso sua empresa precise manter para auditoria e versionamento para ver como era o APP naquela versão você pode manter essa branch em aberto, tendo noção que isso pode aumentar e muito o numero de branches remotas e podendo causar lags ou baguncar a visualizacao de branches remotamente (por exemplo no github, gitlab e etc).