---
aliases: 
tags: 
date created: Thursday, August 22nd 2024, 10:41:41 pm
date modified: Thursday, August 22nd 2024, 10:58:55 pm
---
Quando trabalhamos com o ambiente remoto, temos dois commandos importante, o git fetch e git pull, o git fetch tem a importancia de executar um commando ao qual notifica para você todas as mudancas que tem no remoto ao qual seu repositorio local não tem, todavia ele nao instala os arquivos nem baixa em sua máquina, ele so notifica e sinaliza quais sao os arquivos, branches e commits que faltam em seu computador local.

Se voce dar um git status, podera aparecer que nao ha nenhuma atualizacao na branch, mas nao deixe se enganar por isso, isso se da pois a branch so demonstra atualizacoes somente depois de dar git fetch, e infelizmente o git fetch nao é rodado automaticamente depois de cada commando, com execao de UI's.

---

