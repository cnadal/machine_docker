Cet espace sous github contient les fichiers de bases permettant de mettre en place dans une machine linux (testé sous debian 9++) :

1 - Docker en exécutant le script docker.sh
   
      
      chmod 755 ./get-docker.sh
        
      ./get-docker.sh

2 - La commande docker-compose
    
    
        chmod 755 ./install-docker-compose
    
        ./install-docker-compose
    
    Ce fichier contient la commande suivante
        sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
        
3 - A partir de là , il faut configurer le fichier .env avec votre nom de login car par défaut ce sont des services reliés à cyr qui vont être créés, remplacez <b>cyr</b> par votre Nom, ex pour vivian :

	DB_NAME=testcyr				==> 	DB_NAME=testvivian
	
	PROJECT_NAME=testcyr			==> 	PROJECT_NAME=testvivian
	
	PROJECT_PATH=/var/www/html
	
	MYSQL_USER_NAME=cyr			==> 	MYSQL_USER_NAME=vivian
	
	MYSQL_USER_PASSWORD=toto
	
	MYSQL_ROOT_PASS=root

        
