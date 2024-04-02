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
PARA ELIMINAR EL UTIMO COMMIT DE FORMA DIRECTA

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



------------------------------

SI QUIERES RESETEAR EL HISTORIAL DE LOS COMMITS=>

URL MIRCHA ===> https://jonmircha.com/git#resetear-un-repositorio
cd carpeta-repositorio
mv .git/config ~/saved_git_config
rm -rf .git
git init
git branch -M main
git add .
git commit -m "Commit inicial"
mv ~/saved_git_config .git/config
git push --force origin main
--------------------------
PARA HACER UN USUARIO DE MANERA LOCAL==>

SOLO SE LA PALABRA --LOCAL EN LUGAR DE --GLOBAL

git --version
git config --local user.name "Jonathan MirCha"
git config --local user.email jonmircha@gmail.com
git config --local user.ui true
git config --local init.defaultBranch main
git config --list
# asignando visual studio code como editor de configuración de git
git config --local core.editor "code --wait"
git config --local -e
---------------------------------

PARA COLABORAR==>

FORKEAR EL REPOSITORIO A TU CUENTA ==> 1
CLONAR DE MANERA LOCAL ==> 2
CONFIGURAR EL ORIGEN REMOTO ==> 3{
    RENOMBRE EL ORIGIN POR FORK
    git remote rename origin fork=>1
    AGREGAR EL REMOTO ORIGINAL => 2
    git remote add origin https://github.com/usuario/repositorio.git
}

CREAR UBA NUEVA RAMA=>4
git checkout -b rama-nueva{
    EN ESTA HACES TUS CAMBIOS QUE QUIRES CONTRIBUIR ==>1
    ----
    HACES UN PUSH AL REMOTE FORK==2
    git push fork rama-nueva
}

HACER EL PULL REQUEST EN LA INTERFAZ DE GITHUB===>5

A QUE ORIGIN Y SU RAMA, Y TAMBIEN CON QUE RAMA LOCAL....

----------------------------------------------------
SOLO ADMI DEL REPO ORIGINAL

ACTUALIZAR LOS CAMBIOS DE MANERA LOCAL==>6{
    //ESTO SOLO LA PERSONA ADMINISTRADORA
    git pull==>ASEGURATE DE ESTAR EN LA RAMA MAIN
}

--------------------------------------------------

HACER CAMBIOS EN EL TUYO===7{
    IR A LA RAMA MAIN
    git checkout main
    HACER CAMBIOS PERO EN EL TUYO, PROVINIENTES DEL REPO ORIGINAL
git pull origin main
ACTUALIZAMOS EL REMOTO FORK(DE GITHUB)
git push fork main
ELIMINAR LAS RAMAS NUEVAS 
git branch -d rama-nueva ==> LOCAL
git push fork --delete rama-nueva==> RMEOTA
}