---
aliases: 
tags: 
date created: Sunday, August 18th 2024, 10:47:15 pm
date modified: Thursday, August 22nd 2024, 10:30:11 pm
---
O github não é git, github é uma plataforma open source, onde você pode criar repositórios de código aberto e privado, e com isso pode iniciar desenvolvimento de código colaborativo.

O github contém commandos git para você interagir com o git, e ainda conta com commandos adicionais.

Além do cenário colaborativo, o github por oferecer um servidor em cloud para hospedar o teu código permite uma proteção ainda maior contra surtos em computadores isolados, por exemplo caso algo aconteça ao seu computador pessoal, isso não significa que o projeto inteiro será perdido, ou seja, adicionando uma camada adicional de segurança.

---

# Porque usar github?

- É passível de trabalho colaborativo, principalmente em projetos open source.
- Permite a exposição de seu trabalho, experiência, projetos que você trabalho, quantidade de commits, como você coda e seu perfil, etc e etc.

---

Quando clonamos algo do github, temos a branch main e origin/master, temos essa diferenciação por duas branches para que sabemos onde estamos na master localmente e onde estamos na master de forma remota, isso se da pois fazemos alterações localmente que podem se descompassar com a branch remota, por isso temos esses dois tipos de visualização.

Como eu disse acima, há uma diferenciação entre o remoto e o local, portanto você pode dar checkout entre a branch remota e a branch local, para navegar remotamente basta, dar um checkout no estilo origin/master, fazendo isso, indiferente do que você tenha localmente você vai acessar a master de forma remota. Isso é muito útil para quando você efetua commits na mesma branch localmente mas quer verificar como ela está de forma remota.

Quando voce clona o projeto remotamente, a priori se o projeto tiver mais de uma branch, voce comeca o projeto provavelmente com a master e a main clonada, todavia as branches adicionais não vem em conjunto, e requerem que voce faça o checkout delas remotamente.

Para se navegar para uma branch remota ao qual queremos ter localmente, basta se ter o nome dela e executar o commando git switch <BRANC_DESEJADA>, e ele automaticamente vai ver se existe uma branch remota, e caso positivo ele se conecta come ela.

---

