## 2-1 What are testcontainers?

Les testcontainers sont des bibliothèques qui permettent de lancer des conteneurs Docker temporaires pour exécuter des tests d’intégration réalistes dans un environnement isolé. Par exemple pour executer des tests necessitant un DB sans avoir à en mettre une à disposition

## 2-2 For what purpose do we need to use secured variables ?

Les variables sécurisées sont utilisées pour protéger nos informations sensibles (comme les identifiants Docker) et éviter les fuites d'informations

## 2-3 Why did we put needs: build-and-test-backend on this job? Maybe try without this and you will see!

needs: build-and-test-backend sert à s'assurer que le job ne s'exécute que si les tests passsent. Sinon on aura des images Docker construites avec une appli qui ne compile pas ou ne passe pas les tests.

## 2-4 For what purpose do we need to push docker images?

les images Docker sont push pour les rendre disponibles aux autres membre de l'équipe, sur tout les environnement, pour faciliter le déploiement de l'application.
