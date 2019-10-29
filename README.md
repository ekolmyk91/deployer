Deployer
========

Quick setup wordpress/drupal projects with docker-compose

Installation
------------

## git clone

```
git clone https://github.com/ekolmyk91/deployer.git
```

## Make script globally available

```
sudo mv ~/deployer/deployer /usr/local/bin/deployer
```

## Make script executable

```
sudo chmod +x /usr/local/bin/deployer
```

Deploy new project
==================

## Make project dir
```
mkdir dir ~/Projects/example
```

## Go to the project dir 
```
cd ~/Projects/example
```
## Start deploy
For wordpress
```
sudo deployer new wordpress 
```

For drupal
```
sudo deployer new drupal 
```
After script completion you will see message with your base url, like 
> Your base url example.loc:8000

## Change project name

Open `~/Projects/example/.env` file and set PROJECT_NAME, should be the same as you project dir name, in our case `example`.

## Start docker containers
In your project directory execute next command:

```
sudo docker-compose up -d
```

## Ready to work!

* **Base URL:** http://{PROJECT_NAME}.loc:8000
* **Phpyadmin URL:** http://pma.{PROJECT_NAME}.loc:8000
* **Mailhog** http://mailhog.{PROJECT_NAME}.loc:8000
* **Portainer** http://portainer.{PROJECT_NAME}.loc:8000


## Stop docker containers

```
sudo docker-compose stop
```


Deploy project from repository
==============================

## 1. Go to the project dir 
```
cd ~/Projects/example   
```

## 2. Start deploy (without sudo).
**Attention!** your site should contain example.env and example.docker-compose.yml in work branch.

```
deployer {REPOSYTORY_LINK}
```

## 3. During deploy you will see message:
>Please upload DB .sql file to /home/dev01/Projects/example/database-init

Copy your database .sql file to database-init folder and press Enter.

After docker start, you will need waiting few minutes while database will import. 

## 4. Ready to work!

* **Base URL:** http://{PROJECT_NAME}.loc:8000
* **Phpyadmin URL:** http://pma.{PROJECT_NAME}.loc:8000
* **Mailhog** http://mailhog.{PROJECT_NAME}.loc:8000
* **Portainer** http://portainer.{PROJECT_NAME}.loc:8000







