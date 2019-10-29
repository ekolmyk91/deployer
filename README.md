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
sudo deployer new wordpress 
```
