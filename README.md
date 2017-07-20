# redsen-avs4poc

## Contexte de la preuve de concept
* Application web basé sur SpringBoot
* Persistence avec DB2
* Serveur applicatif Tomcat

## Mode de travail avec REDSEN
* Idéalement revue de conception aux dates suivantes (**Jérémie merci de cocher ce qui est ok pour toi**), online et via repo GitHub:

- [ ] mercerdi 16.8.2017 dés 14:00
- [ ] mercredi 06.09.2017 dés 14:00
- [ ] mercredi 28.09.2017 dés 14:00
- [ ] mercredi 18.10.2017 dés 14:00
- [ ] mercredi 08.11.2017 dés 14:00
- [ ] mercredi 29.11.2017 dés 14:00

## Questions:

### Isolation du domaine
> Décision: aucune invasion dans le domaine autre que java.*, commons.apacche." et les dépendances du domaine
> Du coup, 2 possibilités pour isoler correctement les entités de la persistaence:
> Soit mapping via fichier xml
> Soit couche de mapping (couche application)
