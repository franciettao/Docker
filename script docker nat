#on exécute les mises à jour
sudo apt update && apt full-upgrade -y
#on installe les dépendances
sudo apt install -y apt-transport-https ca-certificates curl gnupg lsb-release
#on ajoute de la clé GPG officielle de Docker
curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
#Ajout du repository Docker dans les sources
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian \
  $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
#on exécute les mises à jour
sudo apt update -y
#on télécharge le paquet Docker depuis les sources
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-compose
# Création du groupe "docker"
# Attribution du groupe à notre utilisateur :
sudo usermod -aG docker $USER

#Active docker au démarrage de l'OS
sudo systemctl enable docker 

#on liste les containers
echo
sudo docker ps 
echo
echo "Test du fonctionnement"
docker run hello-world
