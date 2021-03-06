# redsen-avs4poc

## Contexte de la preuve de concept
* Application web basé sur SpringBoot
* Persistence avec DB2
* Serveur applicatif Tomcat
* Approche BPM (exigences demandées)

## Mode de travail avec REDSEN
* Idéalement revue de conception aux dates suivantes (**Jérémie merci de cocher ce qui est ok pour toi**), online et via repo GitHub:

- [ ] mercredi 16.8.2017 dés 14:00
- [X] mercredi 06.09.2017 dés 14:00
- [X] lundi 25.09.2017 dés 14:00
- [X] lundi 16.10.2017 dés 14:00
- [X] lundi 06.11.2017 dés 14:00
- [X] lundi 27.11.2017 dés 14:00

* Coomit du projet 1/sprint sur github 


## Questions:

### Isolation du domaine
**Décision: aucune invasion dans le domaine autre que java.*, commons.apache." et les dépendances du domaine**

Du coup, 2 possibilités pour isoler correctement les entités de la persistence:
* Soit mapping via fichier xml (hbm.xml) sur le domaine
* Soit couche de mapping (couche application) Entites persistantce <-> Entites Domaines 

> Quel est le choix que tu préconises entre les deux (mapping xml vs mapping objet)?

> Dans le cas du mappiong objet, fw potentiels: http://mapstruct.org/ - MapStruct, http://modelmapper.org/ - ModelMapper, as-tu une expérience dans ce cadre-là?

### Approche BPM
**Décision: utilisation du moteur activiti**

Certaines exigences du POC nécessitent l'utilisation d'un BPM. Relativement léger dans le cadre du POC.

> Le choix de activiti te semble t'il pertinent?

> Nous avions initilement pensé à un outil de machine à état (Spring State Machine), afin de "simuler" le BPM. Que pense tu du choix (à priori abandonné)?

### Découplage front-back
**Décision: application web back sur Tomcat, application front angular 4.x sur serveur WEB (Tomcat, apache ou evt. node)**

> Le choix de node.js te parait-il un bon choix pour un front?

> Ou préferable dépliomenet front avec WAR ?

### Domain Driven Design
""Méthodologie ddd, documentation**

> Comment passer du résulat du travail EventStorming (post it sur tableau) à une modlisation du domaine (entites, vo, aggregats, contexte bornée), --> méthode, article...?

### Couverture de test unitaires

> Quel est le périmètre des test unitaires, pour le domaine --> 100%, ou 50% unitaire et 50% bdd?

> Mock: frameworks/librairies à conseiller?
