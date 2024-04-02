# Curso de git y github


Hola soy Santillan
 
I am making changes, in order to memorize the 4 parts 

El primer comnado tiene que ser===>
git init

GIT ADD==>1
GIT COMMIT==> 2
Git REMOTE ADD  URL DEL REPOSITORIO EN GITHUB==> SOLO UNA VEZ(ANTES DE HACER EL PRIMER PUSH)
GIT PUSH -U RAMA(MASTER / MAIN)==> ESTO SOLO UNA VEZ Y DESPUES DE ESTABLECER LA URL
GIT PUSH=> REMOTO(A LA PLATAFORMA)

GIT PULL=> DEL REMOTO(PLATAFORMA A LOCAL(WORKKING DIRECTORY))

--------------------------------
Puedes Clonar

git close URL DEL REPOSITORIO

--------------------------
CREAR RAMAS 


GIT BRANCH NEW ONE
GIT CHECKOUT ==> TO CHANGE BRANCH

TO

TO MAKE ADD BRANCH TO GITHUB YOU HAVE TO USE ==>
GIT PUSH -U ORIGIN LOCAL-BRANCH
|||

GIT BRANCH CHECKOUT -b NEW AND CHANGE(THIS A SHORTCUT)
---------------------------------------

FUCIONAR RAMAS
GIT MERGE 



--------------------------
AGREGAR MODIFICACIONES A ULTIMO COMMIT

GIT COMMIT --AMEND -NO-EDIT

GIT COMMIT --AMEND -M "NEW MESSAGE"

______________________________________

PARA AGREGLAR CONFICTOS=>

DESPUES DE HACER LO MANUEL DEBEMOS DE GUARDADR  DESPUES AGREGAR UN COMMIT 
1=> GIT ADD .
2=> GIT COMMIT -M "MESSAGE"
3=>ESO ES TODO
-----------------------------------
PARA ELIMINAR EL UTIMO COMMIT 

git reset --hard HEAD~1

----------------------------------

PARA ELIMINAR CAMBIOS CON BASE EL FLUJO
=======>GIT RESET 


git reset --soft

# borra HEAD y Staging
git reset --mixed

# borra todo: HEAD, Staging y Working Directory
git reset --hard

# deshace todos los cambios después del commit indicado, preservando los cambios localmente
git reset id-commit
