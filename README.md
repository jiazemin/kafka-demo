Fichier Docker Compose YAML pour le déploiement d'un cluster Swarm :
1) Sur l'ensemble des machines, exécuter la commande docker swarm init pour créer le master
2) Executer la commande renvoyée par l'étape 1 sur tous les noeuds du cluster (donc tous sauf le master)
3) Créer un network (cluster_network ici) avec la commande docker network create --attachable -d overlay cluster_network`
4) Déployer les services du cluster a partir du docker compose avec la commande suivante docker stack deploy -c docker-compose.yml
5) Enjoy!!
