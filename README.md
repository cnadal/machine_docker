
Ce repo sous github contient les fichiers de bases permettant de mettre en place dans une machine linux (testé sous debian 9++) des services (conteneurs docker)

0 - pour cloner ce repo :
	-- Installer git si nécessaire
	
	apt-get install git
	
	-- Déplacez vous dans un dossier
	
	git clone https://github.com/cnadal/machine_docker.git
	
	-- Cela créera le dossier machine_docker
	
1 - Dans le dossier machine_docker, installer docker avec :
   
      
      chmod 755 ./get-docker.sh
        
      ./get-docker.sh

2 - Dans le dossier machine_docker, installer la commande docker-compose
    
    
        chmod 755 ./install-docker-compose
    
        ./install-docker-compose
    
    Ce fichier contient la commande suivante
        sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
        
3 - Config : à partir de là , il faut configurer le fichier .env avec votre nom de login car par défaut ce sont des services reliés à cyr qui vont être créés, remplacez <b>cyr</b> par votre Nom, ex pour vivian :

	DB_NAME=testcyr				==> 	DB_NAME=testvivian
	
	PROJECT_NAME=testcyr			==> 	PROJECT_NAME=testvivian
	
	PROJECT_PATH=/var/www/html
	
	MYSQL_USER_NAME=cyr			==> 	MYSQL_USER_NAME=vivian
	
	MYSQL_USER_PASSWORD=toto
	
	MYSQL_ROOT_PASS=root

4 - Test : vous pourrez ensuite, exécuter vos conteneurs docker avec la.les instruction.s
  
  	docker-compose build	 	la première fois
	docker-compose up -d		exécute les conteneurs
					web PHP7.4, port 8082
					phpmyadmin, port 8083
					mysql, port 3306
	docker-compose stop		pour stopper les conteneurs
	
	docker ps			pour lister les conteneurs (on peut alors voir id, port et nom des conteneurs)
	docker exec -it testcyr bash	pour exécuter bash dans le conteneur testcyr (changer de nom ou d'id de conteneur cf commande docker ps)
					
	
	
	
