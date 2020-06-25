## ¿Qué comando utilizaste en el paso 11? ¿Por qué?
  
`git reset --hard HEAD~1`
  
## ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
  
`git reflog`
  
Para identificar el commit al que deseo volver. (En mi caso 63ff972)
  
`git reset --hard 63ff972`
  
Para volver al último commit
  
## El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
  
No. `Already up to date` porque styled ya contiene lo único que se hizo en master. La creación de git-nuestro.md
  
## El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
  
Sí, el contenido de git-nuestro.md es diferente en ambas ramas.
  
`nano git-nuestro.md` para resolver el conflicto quedandonos con el contenido de la rama styled.
  
## El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
  
No, styled absorbió a master sin conflictos
  
## ¿Qué comando o comandos utilizaste en el paso 25?
  
Revisé bien qué había en cada rama:
  
`git checkout master`
`git log --graph --pretty=oneline`
`git checkout title`
`git log --graph --pretty=oneline`
`git checkout htmlify`
`git log --graph --pretty=oneline`
  
Junté todo:
  
```
* d6bc553... (HEAD -> title) Añado titulo a git nuestro
*   646370... (HEAD -> master, styled) Merge branch 'htmlify' into styled
|\
| * f740cc... (htmlify) Añado estilo html a git nuestro
* | 63ff97... Estilizado de git nuestro
|/
*   208ac6... Creación git nuestro
```
  
## El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
  
Sí, porque no se deja ningún commit inaccesible.
  
## ¿Qué comando o comandos utilizaste en el paso 27?

`git reflog`
  
`git reset 6463704`
  
## ¿Qué comando o comandos utilizaste en el paso 28?
  
`git restore git-nuestro.md`
  
## ¿Qué comando o comandos utilizaste en el paso 29?
  
`git branch -D title`
  
## ¿Qué comando o comandos utilizaste en el paso 30?
  
`git merge --no-ff d6bc553`
  
Que es el commit donde se quedó 'title' antes de eliminarla.
  
## ¿Qué comando o comandos usaste en el paso 32?
  
`git reset --hard 208ac6a`
  
## ¿Qué comando o comandos usaste en el punto 33?
  
`git reset --hard 1f4d166`
  