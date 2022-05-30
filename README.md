# Symfony-6
Inscription et authentification des utilisateurs 
____________________________________________________________________

Création de l'authentification
Pour créer l'authentification, nous utiliserons la commande

symfony console make:auth

Cette commande va lancer un assistant qui va vous demander de renseigner les informations suivantes :

Le type d'authentification (avec ou sans formulaire de connexion)
Le nom de la classe contenant l'authentification (UsersAuthenticator dans mon exemple)
Le nom du contrôleur qui contiendra les routes de connexion et déconnexion (SecurityController)
La création ou non d'une route de déconnexion (/logout)
Après l'exécution de la commande, les fichiers suivants auront été créés ou modifiés

config/packages/security.yaml
src/Controller/SecurityController.php
src/Security/UsersAuthenticator.php
templates/security/login.html.twig
Création du formulaire d'inscription
Pour créer le formulaire d'inscription sur le site, nous utiliserons la commande

symfony console make:registration-form

Cette commande va lancer un assistant qui va vous demander de renseigner les informations suivantes :

Veut-on ajouter une annotation “@UniqueEntity” dans notre classe Users pour les rendre uniques
Veut-on envoyer un email aux utilisateurs pour activer leur compte
Veut-on connecter automatiquement les utilisateurs après leur inscription
Après l'exécution de la commande, les fichiers suivants auront été créés ou modifiés

config/packages/security.yaml
src/Controller/RegistrationController.php
src/Entity/Users.php
src/Form/RegistrationFormType.php
Nous pourrons ensuite modifier les fichiers en fonction du contexte de notre site.
________________________________________________________________________________________________
users.sql => Base de données : `db_symfony6` =>  Structure de la table `users`
