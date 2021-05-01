# Installer Django et son environement sous linux

Afin de pouvoir faire tourner le site sur votre propre serveur il est conseiller d'utilise python3.9 et son environement virtuel python3.9-venv

Exemple sur linux Ubuntu

pour installer python 
`sudo apt install python3.9 python3.9-venv`


pour installer l'environement virtuel
`python3.9 -m venv monEnv`

pour installer django
```
pip install pip --upgrade
pip install django --upgrade
```
-----------------

# Créer et lancer une application

## Créer
Pour crée une application crée votre dossier par exemple projet_exemple dedans vous créerai la commande suivante
`django-admin startproject config .` la denomination `config .` permet en fait de créer a partir du dossier projet_exemple la structure du code qu'on a denominé config afin d'avoir plus de lisibilité 

## Lancer
La configuration du projet se trouve dans `config/settings.py` pour plus de détail vous pouver prendre exemple sur mon projet. Dedans vous y configurez la base de donnée la timezone la langue toute la structure de base du projet

Pour entrer dans l'environement virtuel ou vous avez installé django il vous faudra faire la commande suivante: 

`. monVenv/bin/activate` votre enviroment sera alors activé.

afin de lancer le code la permiere fois et a chaque changement de base de donnée (objets et administration) il vous sera demandé de faire une migrations sur vote sql, dont les deux commandes sont les suivantes :
```
./manage.py makemigrations
./manage.py migrate
```
le `./manage.py` remplace la commande `python manage.py` 

enfin pour faire tourner le seuveur il vous suffira de faire la commande `./manage.py runserver`
