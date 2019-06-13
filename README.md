# Spring Cloud Exemple

Un exemple de projet spring cloud avec :

* Serveur de configuration (SpringCloudServer)
* Serveur Discovery (Eureka)
* API Gateway
* Docker compose

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

```bash
127.0.0.1 discovery
127.0.0.1 configserver
127.0.0.1 gateway
```

Ensuite, via votre navigateur préféré, vous pouvez tester les urls suivantes:

* http://discovery:8761
* http://configserver:8888/gateway/default
* http://gateway:9000


## Serveur Discovery (Eureka)

- Sert à inventorier les services dans un annuaire (réalise le lien entre host et IP)

http://discovery:8761

## Serveur de configuration (SpringCloudServer)

- Sert à centraliser les configurations des micro-services
- S'enregistre sur le serveur Discovery
- Est sécurisé par Spring Security
- S'appuie sur le file system pour le stockage des configurations (classpath:/configurations) avec native > searchLocations + profiles > active > native

http://configserver:8888

## API Gateway

- Sert de Gateway (proxy Zuul)
- S'enregistre sur le serveur Discovery
- S'appuie sur le serveur de configuration
- Est sécurisé par Spring Security

http://gateway:9000

## 
