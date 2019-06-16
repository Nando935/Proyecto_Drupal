# Composer template for Drupal projects

Este repositorio corresponde al proyecto final del curso Drupal 8. Tiene la intención de ser un sitio web en donde los usuarios puedan subir información relacionada con el CMS. (Aún esta en proceso)

Los reponsables son: Valeria, Adolfo, Fernando

#Clone

git clone https://github.com/Nando935/Proyecto_Drupal.git

#After cloning this project you should do the following 

#Initiate containers:

ddev start

#Install dependencies:

ddev composer install

#Install site using existing config:

ddev exec drush si --db-url=mysql://db:db@db/db --config-dir=../config/sync

#Import config

ddev exec drush cim -y

#Import default content:

ddev exec drush dcdi

