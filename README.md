
----------------------infos doc--------------------

versions symfony : https://symfony.com/releases

bundles symfony :
    https://packagist.org/
    https://flex.symfony.com/


tutoriel api platform :
    https://yoandev.co/integration-continue-dune-api-symfony-api-platform-avec-postman-et-gitlab-ci


----------------------infos commande--------------------

penser a executer wampserver pour acceder a la base de donnee via phpmyadmin

commande pour excuter le serveur web de symfony :
    symfony server:start --port=7070
    Dans son navigateur aller a l adresse : http://127.0.0.1:7070

pour acceder a l'interface pour realiser des requete sur api il faut aller a l'adresse suivante
    https://127.0.0.1:70790/api

commande pour excuter les fixtures :
    cette commande vide totalement la base de données avant d'insérer les nouvelles données:
        php bin/console doctrine:fixtures:load

dans le fichier "composer.json" un script (que j ai nommé « reset-data ») a été crée pour remettre a zero ma base de donnée, surtout utile pour l'utilisation d'un jeu de donnée via des fixtures. Pour l executer il suffit d'executer la commande suivante :
            
            composer reset-data
    
    apres il faudra creer un dossier "migrations" a la racine du projet si il n'existe pas
    puis lancer les commandes suivantes :
        php bin/console doctrine:migrations:generate
        php bin/console make:migration
        php bin/console doctrine:migrations:migrate

----------------------infos project--------------------

20/12/2021 : creation of the project symfony5.4.1

20/12/2021 : entity, fixture, data game

20/12/2021 : dev2 api platiform

20/12/2021 : dev3 jwt avewith api platiform
