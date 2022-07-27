<h1 align="center">Environnement de developpement symfony avec Docker et Docker Compose</h1>

### Outils nécessaires

1. docker et docker-compose
2. Clone : `git clone https://github.com/djessa/symfony-docker.git`
3. Copier le dossier docker et docker-compose.yml dans le racine du projet symfony
4. Vérifier les ports utilisées dans le fichier docker-compose.yml s'ils sont encore disponible
5. Vérifier les noms de volumes dans le fichier docker-compose.yml pour qu'ils soient pas encore utilisées dans un autre projet qui utilise docker.
6. Modifier l'adresse du vhost dans fichier docker/vhost.conf à la ligne 2
7. Modifier le version de l'image php à la ligne 1 du fichier docker/vhost.conf pour qu'il s'adapte à votre projet
8. Modifice le variable d'environnment DATABASE_URL par: DATABASE_URL=mysql://root@db_container_name:3306/db_name

### Exécution de l'application

docker-compose up -d
