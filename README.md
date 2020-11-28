# xi-bootcamp-mobile-pract-git
Repositorio dedicado a la realización de la práctica del módulo de Git en el XI Bootcamp Mobile de KeepCoding.

**José Sancho Monrabal**

jsancho.dev@gmail.com

## Ejercicio 1

### 1- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
```bash
git reset --hard HEAD~1
```
El comando ```git reset HEAD~1``` permite deshacer el último commit, y el modificador ```--hard``` elimina cualquier cambio existente en el _working copy_.

### 2- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
```bash
git reflog
```
```bash
git reset --hard 2b6ffa4
```
Para deshacer lo hecho en el **paso 11**, primero he consultado mediante el comando ```git reflog``` cuál era el identificador del commit en el estado justamente anterior y he podido comprobar que tenía el hash **2b6ffa4** como se puede ver en la siguiente captura:
![alt text](https://github.com/jsmdev/xi-bootcamp-mobile-pract-git/blob/main/images/question-2.png?raw=true)
Conociendo el hash identificativo del commit al que se quiere regresear, a continuación he ejecutado el comando ```git reset --hard``` pasándole como parámetro el hash correspondiente, en este caso el **2b6ffa4**.

Con estos dos comandos he podido deshacer lo deshecho en el **paso 11**.

### 3- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
```bash
git merge main
```
No causó ningún conflicto porque en la rama **_styled_** no había ningún cambio pendiente de commitear.
Además la información de la rama **_main_** ya la tenía la rama **_styled_** y por tanto no se produjo ninguna modificación en el repositorio. El fichero _git-nuestro.md_ se queda como estaba.

### 4- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
```bash
git checkout styled
```
```bash
git merge htmlify
```
Sí que causó un conflicto porque el archivo _git-nuestro.md_ ha sido modificado en las dos ramas que se están fusionando (**_styled_** y **_htmlify_**) y con cambios en las mismas líneas del archivo.

Al haber sido modificadas las mismas líneas de código, _git_ no puede realizar un merge automático porque no sabe que cambios deben prevalecer sobre los de la otra rama.

### 5- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
```bash
git checkout main
```
```bash
git merge styled
```
No, porque la rama **_styled_** comparte el commit común de **_main_** y este no ha sido modificado.

### 6- ¿Qué comando o comandos utilizaste en el paso 25?
```bash
git checkout main
```
```bash
git log --graph --decorate --pretty=oneline
```
![alt text](https://github.com/jsmdev/xi-bootcamp-mobile-pract-git/blob/main/images/question-6.png?raw=true)

### 7- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
```bash
git merge --no-ff title
```
Si, porque la rama **_title_** se encuentra un commit por encima de la rama **_main_** formando el grafo de ambos una lista.

### 8- ¿Qué comando o comandos utilizaste en el paso 27?
```bash
git log
```
![alt text](https://github.com/jsmdev/xi-bootcamp-mobile-pract-git/blob/main/images/question-8.png?raw=true)

y después
```bash
git reset --soft 2b6ffa47662981e605e5eb12894d3a608fa9d757
```

### 9- ¿Qué comando o comandos utilizaste en el paso 28?
```bash
git checkout git-nuestro.md
```

### 10- ¿Qué comando o comandos utilizaste en el paso 29?
```bash
git branch -D title
```

### 11- ¿Qué comando o comandos utilizaste en el paso 30?
```bash
git reset --hard d452835
```
Siendo ***d452835*** el id del commit

![alt text](https://github.com/jsmdev/xi-bootcamp-mobile-pract-git/blob/main/images/question-11.png?raw=true)

### 12- ¿Qué comando o comandos utilizaste en el paso 32?
```bash
git reset --hard d6ee934
```
Siendo ***d6ee934*** el id del commit

![alt text](https://github.com/jsmdev/xi-bootcamp-mobile-pract-git/blob/main/images/question-12.png?raw=true)

### 13- ¿Qué comando o comandos utilizaste en el paso 33?
```bash
git reset --hard d452835
```
Siendo ***d452835*** el id del commit

![alt text](https://github.com/jsmdev/xi-bootcamp-mobile-pract-git/blob/main/images/question-13.png?raw=true)
