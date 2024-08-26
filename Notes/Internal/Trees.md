---
aliases: 
tags: 
date created: Saturday, August 24th 2024, 10:58:05 pm
date modified: Saturday, August 24th 2024, 11:05:04 pm
---
Trees são o objeto do git responsável por guardar o conteúdo de uma pasta. Cada tree pode apontar para blobs e trees subsequentes.

Cada row ou insert de uma tree contem um SHA-1 bash que aponta para um blob ou tree, assim como o modo, tipo, e nome de arquivo.

Ou seja, enquanto o blob é uma estrutura simples, a tree é uma estrutura complexa que define a organizacao do projeto em si por pastas e arquivos.

---

Com essa estrutura permitimos que o git possa navegar entre os commits e manter a estrutura homogenea entre os commits, ja que essas arvores por commit configuram e mostra como o commit organiza a estrutura de arquivos e quais informacoes tem dentro dela.

![[Pasted image 20240824230350.png]]

![[Pasted image 20240824230340.png]]