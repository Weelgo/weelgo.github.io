---
layout : docs_fr
id : TP001
readingEstimation : 20
---

## Workshop : Créez un projet
------------------------

Dans ce travaux pratique, nous allons voir les différentes étapes pour créer le projet suivant :

**Le réseau**

<p align="center">
<img src="reseauCible.png">
</p>

et les indicateurs de pilotage associé :

**Le dashboard**

<p align="center">
<img src="dashboardCible.png">
</p>


**Le gantt**

<p align="center">
<img src="ganttCible.png">
</p>


### Etape 1 : Créez le projet
------------------------

Allez sur votre page d'accueil et cliquer sur le bouton.

<p align="center">
<img src="boutonCreerProjet.png">
</p>

Indiquez un nom et cliquez sur "OK"

### Etape 2 : Créer le réseau
------------------------

Allez sur le réseau en cliquant sur le bouton "Réseau"

<p align="center">
<img src="boutonReseau.png">
</p>

La page vierge du réseau s'affiche. Pour ajouter des actions, cliquez sur le bouton "Editer" 

<p align="center">
<img src="boutonEditer.png">
</p>

Le panel contenant les outils d'édition s'affiche.

<p align="center">
<img src="panelEdition.png">
</p>

#### Ajout d'une action et d'un livrable


Faites un click droit sur l'espace de travail et cliquez sur "Créer action". 

<p align="center">
<img src="menuContextuelCreerAction.png">
</p>

L'action apparait. Renommez la :
* click droit sur l'action.
* renommer.

Nous allons maintenant associé un livrable à l'action: 
* click droit sur l'action.
* Créer livrable.

Vous devez avoir le résultat suivant. 

<p align="center">
<img src="actionLivrable1.png">
</p>

Renommez ensuite le livrable : 
* click droit sur le livrable.
* renommer.

---
**Points importants :**

>*Vous pouvez modifier le type de livrable (neutre, intermédiaire, jalon). Les livrables jalons apparaitront sous forme de coupe. Ils seront affichés dans le dashboard et dans la droite à 45° ainsi que dans la home page du projet.*

---

Continuer à créer les actions et livrables pour obtenir le réseau suivant : 

<p align="center">
<img src="reseauCible.png">
</p>

Pour déplacer les actions et livrables sur l'espace de travail, maintenez le click gauche sur l'item et déplacez les.


#### Créez les repertoires et associez les actions/livrables

Vous avez créé le réseau, nous allons maintenant créer les répertoires : 
* Cliquez sur le bouton "+" 

<p align="center">
<img src="boutonAjoutRepertoire.png">
</p>

* Saisissez le nom du répertoire
* Recommencez pour créer l'arborescence suivante 

<p align="center">
<img src="arborescenceRepertoire.png">
</p>

Une fois les repertoires ajoutés, associez les actions/livrables : 
* Selectionnez les actions et livrable en maintenant le click droit sur l'espace de travail et séléctionnez les actions et livrables. 

<p align="center">
<img src="selectionMultiple.png">
</p>

* Une fois les actions séléctionnées, faites un click droit (maintenir) et dirigé la souris vers le répertoire. 

<p align="center">
<img src="associerReseauRepertoire.png">
</p>

* acceptez l'association. 

Effectuer les même opération pour les actions restantes. Distribué les dans les autres répertoires. 

### Etape 3 : Configurez les actions
------------------------

Le réseau est initialisé, nous allons maintenant configurer les actions. 

Faites un double click gauche sur la première action. Un panel s'ouvre. 

<p align="center">
<img src="panelConfigurationAction.png">
</p>

Dans ce panel, vous pouvez configurer la charge de travail, le responsable, la durée...

Ajouter une charge de travail de 5 jours-homme. 

Cliquer sur le bouton "+" pour modifier le responsable de l'action

<p align="center">
<img src="boutonPlusResponsable.png">
</p>

Renseignez le nom du responsable. S'il n'est pas dans Weelgo, l'application vous proposera de créer un utilisateur virtuel.

<p align="center">
<img src="creerUtilisateurVirtuel.png">
</p>

Vous venez d'initaliser votre première action. 

Continuez à initialiser les autres actions. 

---

**Points importants :**

>*Le responsable par défaut et le responsable du projet ou du répertoire de l'action.* 

>*Les utilisateurs virtuels sont associés au projet. Lors de la création de l'utilisateur, vous pouvez re-utiliser un utilsateur virtuel d'un projet dont vous avez la visibilté.* 

---

### Etape 4 : Configurez le projet. 
------------------------

Cliquez sur l'icone <img src="iconeConfigProjet.png">.

La page du projet s'affiche. Effectuez les opérations suivantes : 
* Renseignez alors la date de début du projet. 
* Ajoutez les calendriers de vos ressources. 

<p align="center">
<img src="configurerProjet.png">
</p>

Pour chaque ressource, définissez :
* le taux de productivité 
* son calendrier en cliquant sur "Ajouter des dates spécifiques"

Quand vous ajoutez des dates spécifiques, le calendrier s'affiche. Vous pouvez alors modifier plus finemenet la productivité en cliquant sur les dates du calendrier. 

<p align="center">
<img src="calendrier.png">
</p>

---

**Tips&Astuces :**
>*Pour modifier une plage, cliquez sur une date puis sur une deuxème date. Une fenêtre s'affichera vous permettant de modifier la plage entre les deux dates.*

---

### Etape 6 : Effectuez un premier snapshots. 
------------------------

Vous venez d'initialiser votre projet. Vous devez maintenant effectuez un snapshot du projet pour avoir une capture du projet à son début. 

Pour cela, cliquez sur le bouton <img src="boutonSnapshot.png"> puis sur "Prendre un snapshot". 

<p align="center">
<img src="prendreSnapshot.png">
</p>

Le snapshot est alors enregistré et disponible. 

<p align="center">
<img src="snapshotPris.png">
</p>



---

**Tips&Astuces :**
>*Pensez à prendre un snapshot du projet régulièrement afin de consolider les indicateurs de pilotage du projet. 

---

### Etape 7 : Partagez le projet à vos collaborateurs
------------------------

Il ne reste plus qu'a partager le projet à vos collaborateurs. Pour cela, aller sur la page principal du projet et cliquez sur le bouton "Partager". 

La page de partage s'ouvre et vous pouvez ajouter vos collaborateurs et configurez les droits. Pour cette partie, je vous invite à lire le tutoriel [ici](http://docs.weelgo.com/fr/tutoriels/partagez_projet/)

<p align="center">
<img src="ecranProjetPartager.png">
</p>


<img src="exemple.gif">


