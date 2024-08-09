---
aliases: 
tags: 
date created: Wednesday, August 7th 2024, 11:26:51 pm
date modified: Thursday, August 8th 2024, 11:35:34 pm
---
# Adicionar ao git ignore e remover de forma retroativa

git rm --cached <nome_do_arquivo>.<extensao_>
git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch <nome_do_arquivo>.<extensao_>' --prune-empty --tag-name-filter cat -- --all


