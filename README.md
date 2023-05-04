# MedHead - Emergency Responder System (ERS)

## Terminologie

### Préfix des applications

Signification des abréviation utilisées.

- **WEB** : Application Web - Application accessible depuis un navigateur web (depuis mobile ou desktop) dans le cas présent).
- **BSNS** : Business Service - Micro-service métier. Regroupe les règles métiers d'un service spécifique (ex : Gestion des patients ou des hôpitaux).
- **TRAN** : Transverse Service -  Micro-service transverse (technique ou business). Peut être amené à exploiter plusieurs services métiers.



### Applications

| ID Application | Nom Application                   | Description                                                  |
| -------------- | --------------------------------- | ------------------------------------------------------------ |
| WEB_ERS        | WebApp - ERS                      | IHM sous forme de WebApp permettant d'accéder aux fonctionnalités de l'ERS |
| BSNS_PMS       | Patient Management Service        | Business service - Création et suivi des informations sur les patients |
| BSNS_EMS       | Emergency Management Service      | Business service - Création et suivi des urgences médicales  |
| BSNS_HMS       | Hospital Management Service       | Business service - Suivi des informations sur les hôpitaux*  |
| TRAN_EDS       | Emergency Dispatcher Service      | Service Transverse - Dispatching et affectations des urgences médicales en fonction du contexte (localisation, spécialité médicale, disponibilités des hôpitaux ...). |
| TRAN_WSS       | WebSocket Server                  | Server WebSocket - Maintient une connexion ouverte avec l'application web en vue de la rendre "reactive" aux événements events |
| TRAN_GWT       | API Gateway - ERS (Traefik based) | API Gateway - Centralise, réécrit et transfère les requêtes aux différents micro-services. |
| ESB_REDIS      | Event Bus Redis                   | Composant Mock basé sur Redis qui permet de pub/sub de message. <br />Exploitera le composant "Event Bus and Data Lake" dans la solution finale. |

