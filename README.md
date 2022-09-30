# TP-LAB01-ISW

Repositorio creado como trabajo práctico para la materia "Ingeniería de Software" de la carrera de 
Ingeniería en Sistemas de Información de la Universidad Tecnológica Nacional - Facultad Regional Santa Fe.

El proyecto consiste de una simple calculadora implementada en Java. Sobre el mismo se realizaron distintas operaciones
a modo de práctica con la herramienta de contorl de versiones Git (implementada en la plataforma GitHub).

# Resolución del enunciado:

2.a) En el workspace del IDE, donde está el proyecto:

Click derecho >> Git Bash Here
```git init
git status
git add .
git commit -am “Commit inicial”
git remote add origin <link al repositorio>
git push -u origin master
```

2.b) El documento “.gitignore” permite declarar los archivos para los cuales no se desea llevar un registro de versiones. En nuestro caso, estamos ignorando la carpeta ```/bin```, en la cual se guardan archivos compilados de java, y la carpeta ```/.settings```, que guarda configuraciones locales de Eclipse.

2.c) y 2.d) Para crear y publicar ramas:
```
git branch Release-#
git checkout Release-#
git push -u origin Release-#
```

2.e) Se modifica el botón ```"Imprimir resultado"``` para que muestre el texto ```"Imprimir resultado copado"``` en la rama develop, luego se crea la rama **Release-1** a partir de la misma.

2.f) Se modifica el botón ```“5”``` para que muestre el texto ```“cinco”```. A través del sitio web de GitHub se crea un “Pull Request” para llevar los cambios de la rama develop a la rama **Release-2**, creada antes de los cambios de 2.e).

2.g) Gitflow indica que se debe realizar un merge de la rama release a la rama master. Una vez realizado (ya sea de manera directa o mediante un PR), la rama **Release-1** es eliminada.

2.h) Se realiza un merge por consola de **Release-2** hacia master, tras eliminar la rama **Release-2** se publica la versión **v1.0.2** mediante la plataforma web.

2.i) A partir de la rama develop se crea la rama **feature-i**, tras publicar los commits “Modificación A” y “Modificación B” se ejecuta:
```
git revert HEAD~0
```
Este comando deshace el último commit realizado.

2.k) Según Gitflow, para llevar a producción los cambios realizados en una rama “feature”, primero se realiza un merge de la rama con develop, luego uno de develop con la rama “release” correspondiente, y finalmente se realiza un merge del release con **master**, eliminando la rama release finalizado el proceso.

3.a) En el documento ```README.md``` se realiza una breve descripción del programa en cuestión. Incluye información sobre el propósito y las razones para utilizar una aplicación, así  como los pasos a seguir y requisitos de instalación, y cualquier otro detalle relevante para quien se encuentre con el software documentado por primera vez.
3.b) Para aprobar un “Pull Request” puede esperarse que quien proponga cambios realice una breve descripción de los mismos, las razones para implementarlos y las implicaciones de llevar tales modificaciones a producción. GitHub provee herramientas para visualizar los cambios propuestos, resaltando las líneas de código modificadas y, en caso de generarse conflictos, permitiendo seleccionar qué cambios conservar y cuales descartar para un único PR.

