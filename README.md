# Spring Cloud Exemple

Un exemple de projet spring cloud avec :

* Serveur de configuration (SpringCloudServer)
* Serveur Discovery (Eureka)
* API Gateway

## Serveur Discovery (Eureka)

Sert à inventorier les services dans un annuaire (réalise le lien entre host et IP)

## Serveur de configuration (SpringCloudServer)

Sert à centraliser les configurations des micro-services
S'enregistre sur le serveur Discovery
Est sécurisé par Spring Security

## API Gateway

Sert de Gateway
S'enregistre sur le serveur Discovery
S'appuie sur le serveur de configuration
Est sécurisé par Spring Security

## 
