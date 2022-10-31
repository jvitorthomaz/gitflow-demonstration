# Demonstração simples de Fluxo de trabalho com GitFlow para treinamento.

## Passos antes de iniciar a demonstração com GitFlow:

* Criar projeto com GitHub
* Clonar projeto para sua máquina. Na demonstração foi clonado pelo VS Code.
* Criar arquivos para demonstração. Para a demonstração foram criados dois arquivos, o index.html  e o cart.html
* Executar os seguintes comandos Git:
   * git add .
   * git commit -m "páginas iniciais foram criadas"
   * git push

## Inicio da simulação com GitFlow:


* ### BRANCH DEVELOP

0. git checkout -b develop  (Criar e acessar a branch develop)
1. git push

* ### BRANCH FEATURE

2. git checkout -b feature/contato  (Criar e acessar a branch feature/contato)
3. git push

4. Criar arquivo contato.html

5. git add .  
6. git commit -m "página de contato criada" 
7. git push 

8. git checkout develop (volta para a branch develop)

9. git merge feature/contato  (faz merge com a branch feature/contato)
10. git push			

11. git branch -d feature/contato (deletar branch feature/contato)

* ### BRANCH RELEASE

12. git checkout -b release/1.1.0 (Criar e acessar a branch de release)
13. git push

14. git tag v1.1.0  (aplica uma tag nela)
15. git push --tags

16. git checkout develop  (Volta para a branch de develop)

17. git merge release/1.1.0 (Faz merge com a branch release/1.1.0)
18. git push

19. git checkout main (volta para a branch main)

20. git merge release/1.1.0 (Faz merge da main com a release)
21. git push

22. git branch -d release/1.1.0 (Deletar branch de release)


* ### BRANCH HOTFIX

23. git checkout -b hotfix/1.1.1  (Criar e acessar branch de hotfix)
24. git push

25. git tag v1.1.1  (aplica uma tag nela)
26. git push --tags

27. git checkout main (Voltar para branch main)

28. git merge hotfix/1.1.1  (Faz merge da hotfix na master)
29. git push

30. git checkout develop  (volta para a develop)

31. git merge hotfix/1.1.1  (faz merge da hotfix com a develop)
32. git push

33. git branch -d hotfix/1.1.1  (deletar branch de hotfix)


**Fluxo GitFlow:** https://www.alura.com.br/artigos/assets/git-flow-o-que-e-como-quando-utilizar/imagem3.png

A demonstração  foi realizada com os comandos básicos do Git. Também é possível fazer com a CLI do GitFlow. Conteúdo teórico para quem deseja entender mais sobre Gitflow:
https://www.alura.com.br/artigos/git-flow-o-que-e-como-quando-utilizar

