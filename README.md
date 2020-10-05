Cet espace sous github contient les fichiers de bases permettant de mettre en place dans une machine linux (testé sous debian 9++) :

1 - Docker en exécutant le script docker.sh
    Pour ce faire :
        chmod 755 ./get-docker.sh
        ./get-docker.sh

2 - La commande docker-compose
    Pour ce faire :
    chmod 755 ./install-docker-compose
        ./install-docker-compose
    
    Ce fichier contient la commande suivante
        sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
        
        
        
