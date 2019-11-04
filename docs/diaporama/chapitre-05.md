<!-- .slide: data-background-image="images/insee_ensai.png" data-background-size="600px" class="chapter" -->

## 5

<h1>Application de gestion de spécification</h1>

%%%

<!-- .slide: class="slide" data-background-image="images/insee_ensai.png" data-background-size="600px" -->

### Choix de l'architecture

#### Architecture "classique" de type client-serveur Web

#### Communication par l'intermédiaire du protocole http au travers d'une API

#### Respect de l'environnement applicatif de l'Insee

<div class="center">
	<img src="images/appli-back.jpg" width="600px" />
</div>

%%%

<!-- .slide: class="slide" data-background-image="images/insee_ensai.png" data-background-size="600px" -->

### Le Front-Office : technologie JavaScript

<div class="center">
	<img src="images/js.png" width="200px" />
</div>

Application vu par le client, visuel, faite pour intéragir avec le client :

- Interface graphique en JavaScript
- Utilisation des libraries React et Redux
- Ecriture des composants avec React et JSX
- Gestion de l'état de l'application avec Redux

%%%

<!-- .slide: class="slide" data-background-image="images/insee_ensai.png" data-background-size="600px" -->

### Fonctionnement du front-office

<div class="center">
	<img src="images/diag_redux_final.jpg" width="800px" />
</div>

%%%

<!-- .slide: class="slide" data-background-image="images/insee_ensai.png" data-background-size="600px" -->

### Le Back-Office

Application hebergée côté serveur, n'est pas accessible directement par le client, s'occupe des traitements.
Elle respecte une architecture en 3 couches fonctionnelles :

- Couche web-services : l'API
- Couche de services : les traitements
- Couche de persistance : la base de données

%%%

<!-- .slide: class="slide" data-background-image="images/insee_ensai.png" data-background-size="600px" -->

### Fonctionnement du back-office

<div class="center">
	<img src="images/diag_back_office_service.jpg" width="800px" />
</div>

%%%

<!-- .slide: class="slide" data-background-image="images/insee_ensai.png" data-background-size="600px" -->

### Les bénéfices obtenus grâce au découpage du Back-Office

Le développement en couches permet d'obtenir :

- une forte cohérence au sein d'une couche
- un faible couplage entre les couches
- une grande modularité

**Les bénéfices :**

- Cela permet de développer plus facilement, plus rapidement
- le code est beaucoup plus lisible et maintenable par une autre personne
- on peut facilement ajouter de nouvelles fonctionnalités car c'est bien découpé

%%%

<!-- .slide: class="slide" data-background-image="images/insee_ensai.png" data-background-size="600px" -->

### Le module de comparaison de version

Le module permettant de comparer plusieurs versions du document de spécification est intégré dans l'application.
Cette comparaison est faite dans le langage Java dans la partie back-office de l'application.

La comparaison étant maîtrisée, on peut personnaliser l'affichage :

<div class="center">
	<img src="images/modif.jpg" width="600px" />
</div>
