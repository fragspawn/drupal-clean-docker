# Docker Drupal Drush and Composer

Build a microservices instance of Drupal as a start point for any project 

## Setup

* create an .env file for: DBH, DB, DBU, DBP, DP, DH for credentialling
* run docker-compose up
* open browser to http://localhost:8888
* login with user 'admin' and the password from .env DP

## Continuous improvment

enter drupal-www with 'docker exec -it drupal-www /bin/bash' and
composer update or composer include <package>

## security

Whilst its not recommended to run this outside dev, one should disable the 'drupal-phpmyadmin' container on staging
 
## going forward
* A better script outside docker-compose is required to upgrade schema on instantiation
* depends_on in docker-compose not working, find a better solution for drupal to wait for db to come up
* .gitignore over 3rd party themes and modules probably not a good idea if editing is necessary 

