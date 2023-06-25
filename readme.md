## Ej.1 Siguiendo el trazo

**¿Qué comando utilizaste en el paso 11? ¿Por qué?**
> `git reset --hard HEAD~1` : Este comando mueve el puntero HEAD (y la rama actual si estás en una) al commit previo, en 
este caso HEAD~1 se refiere al commit previo. La opción --hard hace que todos los cambios en tu working copy también sean 
revertidos a este estado. 

**¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**
Si sólo se refiere al commit (sin recuperar el workinCopy), entonces uso git reflog y git reset --hard [SHA] para 
volver al estado del commit.
> `git reflog` : para ver el registro de las acciones recientes. En este log, encuentro el SHA del commit 
que deshice.
> `git reset --hard 7136734` :  Esto moverá el puntero HEAD (y también el puntero de la rama "styled") al commit 7136734, 
volviendo a este estado del proyecto. 

**El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**
No causó conflicto porque para que se diera un conflicto de merge en git, las mismas partes del código tendrían que ser 
modificadas de manera diferente en las dos ramas que se intentan combinar, y no es el caso.

**El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**
`CONFLICT (content): Merge conflict in git-nuestro.md  
Automatic merge failed; fix conflicts and then commit the result.`
> Las mismas partes del código intentan ser modificadas de manera diferente en las dos ramas que se intentan combinar

**El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**
> No. En este punto, la rama main ahora tiene todos los cambios que había hecho en la rama styled. El mensaje 
"Fast-forward" significa que Git pudo hacer un merge simple, avanzando la rama main a donde está styled, ya que no había 
cambios en main que no estuvieran en styled.

**¿Qué comando o comandos utilizaste en el paso 25?**
> `git config alias.graph "log --branches --graph --oneline"`
> `git graph`

**El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**
> Si. En este caso, todos los commits de la rama "title" están por delante de los commits de "main", lo que significa que 
la rama "main" puede avanzar para ponerse al día con "title", lo que se conoce como "fast-forward".

**¿Qué comando o comandos utilizaste en el paso 27?**
Podría haber usado `git log` para encontrar el commit que buscamos y luego `git reset --soft <commit>` para deshacer el 
merge ejecutado. `--shoft`mantendrá los cambios en el workingCopy. Pero como es el inmediatamente anterior. 
>`git reset --soft HEAD~1` para referir al commit inmediatamente antes del commit actual. Esto llevará un commit atrás, 
manteniendo los cambios en tu working copy y en el índice.

**¿Qué comando o comandos utilizaste en el paso 28?**
> `git restore --staged git-nuestro.md` : para descartar cambios que están en la staging area.
> `git checkout -- git-nuestro.md` : para descartar cambios en workingCopy

**¿Qué comando o comandos utilizaste en el paso 29?**
> `git branch -d title`

**¿Qué comando o comandos utilizaste en el paso 30?**
> `git merge 73ef31c`

**¿Qué comando o comandos usaste en el paso 32?**
> `git checkout 295a580`

**¿Qué comando o comandos usaste en el punto 33**?
> `git checkout 5f9f721`

