# Spring Cloud Exemple

Un exemple de projet spring cloud avec :

* Serveur de configuration (SpringCloudServer)
* Serveur Discovery (Eureka)
* API Gateway

## Installation

Se placer dans le dossier

```bash
mvn clean install
```

## Docker

Se placer dans docker

```bash
docker-compose up
```

### Exécution en local et tests

```bash
sudo nano /etc/hosts
```

Ajouter:

127.0.0.1 dicovery
127.0.0.1 configserver
127.0.0.1 gateway

Ensuite, via votre navigateur préféré, vous pouvez tester les urls suivantes

http://discovery:8761
http://configserver:8888/gateway/default
http://gateway:9000


## Serveur Discovery (Eureka)

Sert à inventorier les services dans un annuaire (réalise le lien entre host et IP)


## Serveur de configuration (SpringCloudServer)

Sert à centraliser les configurations des micro-services
S'enregistre sur le serveur Discovery
Est sécurisé par Spring Security

## API Gateway

Sert de Gateway
S'enregistre sur le serveur Discovery
S'appuie sur le serveur de configuration
Est sécurisé par Spring Security

## 
