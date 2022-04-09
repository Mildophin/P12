# Projet 12 du parcours python d'OC : Epic Events
Ce programme s'agit d'une API réalisée avec Django pour une société fictive d'évènementiel appelée Epic Events.  
L'application permet de gérer des clients, contrats et événements via une API REST et une interface d'administration.  
Ce projet a été réalisé dans le cadre du parcours python d'OC. 

## Fonctionnalités

Tout les endpoints sont décrit dans la [documentation](https://documenter.getpostman.com/view/14877827/UVyxRZuz). 

## Processus d'installation et lancement de l'application

Premièrement, il faut installer Python.  
Puis ouvrez la console, placez-vous dans le dossier (/cd) souhaité puis clonez ce dossier :
```
git clone https://github.com/Mildophin/P12.git
```
Ensuite, placez-vous dans le dossier P12, puis créez un nouvel environnement virtuel :
```
python -m venv env
```
Par la suite, activez-le :

Sur Windows :
```
env\scripts\activate.bat
```
Sur Linux :
```
source env/bin/activate
```
Installez ensuite les packages requis :
```
pip install -r requirements.txt
```
Enfin, il vous faut une base de donnée afin de pouvoir lancer le projet, il ne vous reste plus qu'à installer 
postgreSQL et créer une base de donnée vierge, puis de la connecter en mettant les bonnes informations dans le 
fichier settings.py.  

Prochaine étape, placez-vous à la racine du projet (là où il y a le fichier manage.py), puis faites les migrations :
```
python manage.py makemigrations
```
Puis un migrate : 
```
python manage.py migrate
```
À présent il vous faut lancer le serveur : 
```
python manage.py runserver
```
C'est finit ! Maintenant, vous pouvez utiliser l'application grâce aux différents endpoints détaillés dans la 
documentation.  

N'oubliez pas d'assigner les utilisateurs aux groupes correspondant à sales_members, support_members ou 
management_members que vous aurez créé afin que les permissions fonctionnent bien.
