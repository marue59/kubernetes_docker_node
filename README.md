# Comment utiliser l'application ?

### Dockerizer l'application

Pour Dockerizer l'application, il faut, dans un terminal ouvert à la racine du projet, exécuter les commandes ci-dessous: 

```bash
docker build -t nom-repo/nom-image:latest .
```

Pour la tester en local, on peut lancer un conteneur de l'application avec cette commande: 

```bash
docker run -d -p 3000:3000 -e STORY_FOLDER=story -v /app/story nom-repo/nom-image
```

Enfin, pour la mettre sur DockerHub, il faut, après s'être logué avec `docker login`, exécuter la commande ci-dessous: 

```bash
docker push nom-repo/nom-image
```