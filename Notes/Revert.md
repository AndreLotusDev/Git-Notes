---
aliases: 
tags: 
date created: Sunday, August 18th 2024, 10:27:23 pm
date modified: Sunday, August 18th 2024, 10:36:12 pm
---
A diferença entre o git reset e git rever é que o git revert preserva o histórico, enquanto o git reset de fato apaga os commits e volta o ponteiro da branch para alguns commits atrás e remove rastros, o git revert volta o estado do arquivo para alguns commits anteriores, mas dentro de um novo commit, tanto é que é perguntado o nome do novo commit quando o commando é executado.

git revert <COMMIT_HASH> - Reverte as coisas para esse commit, e joga um espelho negativo do estado do arquivo para um novo arquivo.

O commando git revert pode pedir resolução de conflitos, já que as vezes o git pode se perder durante o revert.

PS: O git revert é mais aconselhado para empresas ou fluxos onde é necessário manter como processo de auditoria o commit desastroso, não se perdendo assim hora nenhuma o histórico do git...

Outro ponto a se considerar é que quando você já pushou os commits para o remoto, o reset é dificil de set feito, uma vez que quando você executa o git reset e da um push --force reescrevendo o historico da branch, outras pessoas precisam fazer o mesmo, o que exige comunicação e coordenção, e caso alguém não faça e suba uma nova alteração, pode conflitar ainda mais, ou seja, a orquestração é muito essential em cenários de git reset com o conteudo ja em remoto, o que não é o mesmo cenário para o git revert, ao qual preserva a estrutura original da branch.