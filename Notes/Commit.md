---
aliases: 
tags: 
date created: Tuesday, July 16th 2024, 7:07:51 pm
date modified: Monday, August 5th 2024, 10:52:05 pm
---
Commits são checkpoints de seu projeto, onde o seu projeto é versionado propriamente.

Um commit, diferente de salvar um arquivo, pode salvar varios arquivos de uma vez, em vez de pensar como um salvamento de arquivos, podemos pensar no commit como um checkpoint geral do projeto.

É recomendado nunca commitar tudo de uma vez, por convenção e boas práticas sempre devemos commitar de forma atomica as coisas, segmentando, por fix, feature, tornando assim as coisas mais granulares.

A documentação official do git recomenda a gente quando commitar as tarefas usar present tense, todavia isso é recomendação official do git, mas nada lhe impede de usar metodos diferentes, por exemplo a comunidade do stackoverflow sempre debate entre past tense vs present tense. Eu pessoalmente prefiro past tense como por exemplo: "[Fix] - Arrumado sistema de arquivos e salvamento", já que se for parar pra pensar, eu fiz uma fix ao qual está no passado, o código não é presente, mas sim feito em um passado próximo (ou não tão próximo).

---

Quando commitamos algo temos duas opções:

Ou podemos executar o commando git commit -m "Mensagem desejada" ao qual fara um commit direto.

Ou podemos fazer git commit, esse segundo commando ele vai abrir um editor externo, só há necessidade de se tomar cuidado, tendo em vista que ele vai abrir caso você não tenha configurado manualmente o VIM. O que torna díficil a escrita da mensagem de commit.

Esse segundo commando é útil quando a mensagem de commit é maior do que o usual, isso se dá pois ele abre um editor externo permitindo comentários de multiplas linhas, diferente do primeiro commando, muito útil em empresas grandes ou que exigem documentação externa.

---

Todo commit aponta para o commit anterior, fazendo uma estrutura de dados de fila.