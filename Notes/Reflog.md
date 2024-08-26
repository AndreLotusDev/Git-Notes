---
aliases: 
tags: 
date created: Saturday, August 24th 2024, 11:28:07 pm
date modified: Monday, August 26th 2024, 8:24:35 pm
---
O reflog é o historico do historico do git, ele aponta todas as mudancas dentro das branches, cada mudanças aplicadas dentro dela o git mantém.

Nos podemos visualizar, ou atualizar esses logs usando o commando git reflog.

Ele trackeia mudancas entre HEAD, branches e tags.

Ele mantem o historico de coisas feitas mesmo que voce tenha refeito ou deletado tal coisa.

O diretorio para o reflogs é: .git/logs

PS: Os logs do reflog literalmente grava tudo que voce faz, e ele mantem esse texto nao criptografado e de forma descomprimida.

Os reflogs sao locais, isso se deve pois não faz sentido você manter reflogs de outros desenvolvedores, principalmente em projetos grandes com milhares de desenvolvedores, imagina como seria seu reflog, seria simplesmente 'overwhelming'.

Os reflogs também expire, isso significa que o git limpa os entries mais antigos e isso é totalmente configurável, como por exemplo você pode configurar que entries com mais de 90 dias devem set removidos.

---

**Por que o git reflog é útil?**

- **Recuperação de commits:** Se você acidentalmente excluir um commit, o git reflog pode te ajudar a recuperá-lo.
- **Entendimento da história do projeto:** Ao analisar o git reflog, você pode entender melhor como o projeto evoluiu ao longo do tempo.
- **Depuração:** Se você estiver tendo problemas com o seu código, o git reflog pode te ajudar a identificar o ponto em que as coisas começaram a dar errado.

---

PS: Se voce executar um git reset --hard, ele ira desfazer o commit e deletar ele da branch, todavia voce ainda tera ele no git reflog, portanto para desfazer o reset basta executar um git reset --hard master@{1}, e assim iremos recuperar o commit "perdido".