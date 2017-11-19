---
layout : docs_fr
title : Créer et gérer un projet sous Weelgo
description : Dans ce tutoriel, vous apprendrez à créer un projet Weelgo 
toc : true
---

## Introduction

Ce tutoriel s'adresse aux personnes souhaitant piloter un projet via l'outil Weelgo. Au travers de ce tutoriel, nous rappelerons certains grands principes de gestion de projet. Nous vous fournirons aussi une méthodologie vous permettant de structurer et démarrer votre projet en toute maitrise ! 

La modélisation d'un projet Weelgo s'effectue en 5 étapes. 

__[Etape 1 : Modéliser son projet](#modeliserProjet)__
+ [Définition des actions et des livrables](#definitionActionsLivrables)
+ [Ordonnancement des actions](#ordreActions)
+ [Définition des répertoires](#repertoire)

__[Etape 2 : L'organisation opérationnel du projet](#organisationProjet)__
+ [Ajout des tickets](#ajoutTickets) 
+ [Affectation des responsables](#affectationResp)
+ [Partage du réseau](#partageReseau)
+ [Renseignez des charges de réalisation](#chargeReal)

__[Etape 3 : Analyse du déroulement logique du projet](#analyseLogique)__

<a id="modeliserProjet"></a> 
__[Etape 4 : Définition des hyopthèses de départ ( date de début et calendrier des ressources )](#hypoDepart)__

__[Etape 5 : Analyse du planning et des indicateurs](#analysePlanning)__


<a id="definitionActionsLivrables"></a> 
## Etape 1 : Modéliser son projet 


*Vue Weelgo : Réseau*

### Définition des actions et des livrables

Un projet est un enchainement d'actions aboutissant à un ou plusieurs livrables. La modélisation du projet consiste donc à : 
* Déterminer l'ensemble des livrables constituant le projet
* Déterminer les actions permettant d'aboutir à ces livrables

Cette succession d'action / livrable fomera votre réseau. Le réseau étant la colonne vertebrale de votre projet.


Ces livrables peuvent être de 3 types. Des livrables neutres, intermédiaire ou de type jalon 

<p align="center">
<img src="/fr/img/typeLivrable.png">
</p>

Les livrables jalons sont des livrables que vous souhaitez suivre particuliérement. Ils apparaitront dans le tableau de bord du projet et bénéficieront d'un suivi particulier. 


Pour chaque action, il est nécessaire de se poser les questions suivantes :
* Que dois-je faire pour réaliser cette action? 
* Quel sont les inputs nécessaires à la réalisation de cette action? 
* Qu'ai-je en sortie de mon action ? 


Gardez en mémoire que vous avez la possibilité de saisir des tickets dans actions ( depuis la vue Organisation ). Un choix structurel s'impose donc. Dois-je créer une action ou un ticket? 

Pour vous aidez dans votre choix, dites-vous que le réseau doit matérialiser la structure de votre projet. Notamment avec la liste des livrables de votre projet. Si le résultat du ticket et un livrable de haute importante ( application, documentation... ), une action est préférable. Dans le cas contraire, privilégiez le ticket.

Some basic Git commands are:
```
git status
git add
git commit
```ruby

---

**Nos préconisations :**
<a id="ordreActions"></a> 
>*Le réseau doit être structuré par des actions fournissant des livrables clés. Une action n'aboutissant pas à un livrable de haute importance doit plutot être traitée comme un ticket ( depuis la vue Organisation ).*

**Points importants :**

>*Une action doit forcement aboutir à un livrable ou plusieurs livrables. Une action n'aboutissant à aucun résultat ( livrable ) ne doit âs être présent dans le réseau.*

---

### Ordonnancement des actions


L'ordonnancement  permet de mettre en ordre l'ensemble des actions. Nous déterminons ainsi les dépendances entre chaque action et leur chronologie.

La solution Weelgo propose 2 type d'ordonnancement. L'ordonnancement "physique" et l'ordonnancement "temporel". 

L'ordonnancement "physique" est le lien entre 2 actions reliées par un livrable. L'action B attendant le livrable de l'action A afin de commencer.

<p align="center">
<img src="/fr/img/actionLienPhysique.png">
</p>

L'ordonnancement "temporel" correspond à une dépendance temporelle entre 2 actions. L'action B ne pouvant commencer uniquement quand l'action A est terminée. Néanmoins, le livrable de l'action A n'est pas nécessaire à la réalisation de l'action B.

<p align="center">
<img src="/fr/img/actionLienTemporel.png">
</p>

Dans weelgo la définition des actions et l'ordonnancement s'effectue en même temps. En effet, lors de la modélisation de votre projet, vous allez naturellement enchainer les actions / livrables pour aboutir au résultat final.  

Lors de la création du réseau, il est nécessaire de considérer les ressources comme infinies. Cela permettra de connaitre le délai minimum possible avec le maximum de parallélisme ).

<p align="center">
<img src="/fr/img/reseau.png">
</p>

---

**Nos préconisations :**
<a id="repertoire"></a> 
>*Ordonnancez votre projet sans prendre en compte les ressources ( ressources infinie ). Vous connnaitrez le délai minimum de réalisation de votre projet et vous pourrez déterminer le nombre maximum de personne pouvant être affecté sur votre projet sur les différentes phases.*

---

### Définition des répertoires 

Suite à la création du réseau, il est nécessaire de finaliser sa construction en l'encapsulant dans une structure. Cette structure, ou découpage, permettra de faciliter la compréhension et la gestion au quotidien du projet.

De nombreux critères peuvent être utilisés pour effectuer ce découpage : 

* Fonctionnalités ( mesurer, asservir )
* Sous-ensembles physiques ( boitier A , boitier B ) 
* Responsabilités industrielles ( sous-traitant X, service Y ) 
* Types de tâches ( Etude, réalisation ) 
* Spécialités techniques ( mécanique, logiciel ) 
* Ressources ( Ingénieurs, Techniciens, Outillages ) 
* Coûts ( devis 1, achat K, sous-traitance X ) 
* Maintenance ( éléments échangeables, ordre du démontage ) 
* Documentation ( Spécifications, Dossiers, Procédures )

Ce découpage est matérialisé par la création de répertoires et de sous répertoires dans la vue "Réseau".

<p align="center">
<img src="/fr/img/repertoire.png">
</p>

Nous retrouvons ici deux types de découpages. Un premier découpage de haut niveau correspondant à un découpage en type de taches ( Mise en place, Développement ), et un découpage par ressource au niveau de la phase de développement. 

Il est possible de descendre de niveau si nous estimons cela nécessaire.  Ici nous avons, pour chaque ressource, effectué un découpage fonctionnel. 

<p align="center">
<img src="/fr/img/repertoire2.png">
</p>


Ces répertoires contiendront les différentes actions nécessaire à la réalisation de votre projet. 

Cette architecture permet, d'avoir une vision globale de la réalisation du projet. Bien évidemment, il est possible de modifier l'affectation du découpage fonctionnelle en fonction des contraintes rencontrées lors de la réalisation du projet. 

De plus, l'ajout d'actions dans les répertoires permet d'afficher le réseau avec des niveaux de détail différents. 

__Affichage haut niveau__

<p align="center">
<img src="/fr/img/reseauHautNiveau.png">
</p>

__Affichage niveau intermédiaire__

<p align="center">
<img src="/fr/img/reseauNiveauIntermediaire.png">
</p>

__Affichage complet__ 

<p align="center">
<img src="/fr/img/reseauComplet.png">
</p>

Pour affecter des actions à un répertoire, il suffit de sélectionner les actions et tracer un trait vers le répertoire souhaité. 

( mettre GIF )

---
<a id="organisationProjet"></a> 
**Nos préconisations :**

>*Effectuez des découpages simples. Au plus proche de la réalité. Des découpages complexes peuvent compliquer la gestion de votre projet.*

---



## Etape 2 : L'organisation opérationnel du projet. 

*Vue Weelgo : Organisation*

La vue Organisation de Weelgo représente le projet sous une forme hierachique ou WBS ( Work Breakdown Structure ). C'est à dire un organigramme des actions du projet. 

Cet organigramme est construit de la manière suivante : 
+ Les répertoires correspondent aux différents niveaux du WBS
+ Les actions correspondent au niveau le plus bas. 


Projet :

<p align="center">
<img src="/fr/img/reseau.png">
</p>

Vue WBS : 

<p align="center">
<img src="/fr/img/vueWBS.png">
</p>

<a id="ajoutTickets"></a> 
Vous allez donc pouvoir finaliser l'organisation de votre projet en ajoutant :
+ Les tickets associés aux actions
+ Ajouter des responsables
+ Ajouter des charges de réalisation 


### Ajout des tickets

Dans Weelgo, les tickets sont obligatoirement rattachés à une action. Les tickets doivent être considérés comme une décomposition plus fine de l'action ( comme une TODO list ). 

Ils peuvent être créés en cliquant sur <img src="/fr/img/iconeAjoutTicket.png">. Ils peuvent être déplacés ( via du drag&drop ) dans la liste des tickets ou dans d'autres actions. 

Le livrable etant rattaché à l'action, les tickets n'aboutissent pas à un livrable dans Weelgo. Néanmoins, ils ont des caractéristiques communes. Vous pouvez affectez des responsables aux tickets ainsi que des charges de réalisation. 

Les tickets sont priorisés de haut en bas. Les tickets situés le plus en haut sont plus prioritaires que les tickets en dessous.

<p align="center">
<img src="/fr/img/prioriteTickets.png">
</p>

 
---

**Nos préconisations :**

>*Considérer les tickets comme la TODO list de l'action.* 
<a id="affectationResp"></a> 


**Tips&Astuces :**
>*Un ticket sans charge de réalisation peut être géré comme un ticket avec une charge. Néanmoins il apparaitra pas dans les vues de planification.* 

<p align="center">
<img src="/fr/img/ticketAvecCharge.png">

<img src="/fr/img/ticketSansCharge.png">
</p>



---

### Affectation des responsables

L'affectation des responsables permet de transmette la responsabilité de l'action à un collaborateur. 

Pour cela, trouvez votre collaborateur depuis le bouton <img src="/fr/img/boutonRessource.png"> et cherchez le depuis la recherche. 

<p align="center">
<img src="/fr/img/affectationRessource.png">
</p>

Une fois séléctionné, il suffit d'affecter ( drag&drop ) la personne à une action ou à un ticket. 

( mettre image / GIF )

---
<a id="partageReseau"></a> 
**Nos préconisations :**
>*Affectez un responsable unique à une action.*
<a id="chargeReal"></a> 

**Tips&Astuces :**
>*Si l'action contient plusieurs responsable. Nous considérons que l'action sera réalisée par l'ensemble des collaborateurs en même temps ( en fonction de leurs disponibilités ). La charge de réalisation sera alors distribuée entre tous les responsables.* 

---

### Partage du réseau

Le partage du réseau peut s'effecuter à tout moment. Pour cela, il suffit de cliquer sur le bouton partage : 

<p align="center">
<img src="/fr/img/partage.png">
</p>


Nous vous conseillons d'effectuer ce partage une fois que vous avez indiqué l'ensemble des responsables du réseau pour les raisons suivantes :  
+ Une fois le réseau partagé, vous pouvez réunir votre équipe afin de discuter du déroulement à venir du projet
+ Vous allez pouvoir expliquer les actions à réaliser et ainsi donner la main aux responsables de renseigner les charges de réalisation

---
<a id="partageReseau"></a> 
**Nos préconisations :**
>*Partagez le réseau après avoir effectué les affectations des responsables. *
<a id="chargeReal"></a> 

**Tips&Astuces :**
>*Vous pouvez partager le réseau à tout moment. De plus vous pouvez créer une URL cryptée afin de partager le réseau à des membres extérieurs au projet et non inscrit sur Weelgo.* 

---

### Renseignez des charges de réalisation


Lors de cette étape, vous devez indiquer la charge de réalisation des actions et des tickets.

Attention à ne pas confondre la durée de réalisation d'une action et la charge de réalisation de l'action

La charge de réalisation correspond au temps nécessaire de réalisation de l'action. La durée de réalisation correspond au temps que prendra la réalisation de la charge de l'action. 

Exemple : 

Une action de 5 jh peut etre réalisé en 10 J. 
Charge de réalisation : 5 jh
Durée de réalisation : 10J

**Une action / ticket peut être plannifié uniquement si une charge de réalisation est renseignée.** 

L'affectation des charges des actions s'effectuent depuis la vue "Réseau" 

<p align="center">
<img src="/fr/img/affectationChargeAction.png">
</p>

L'affectation des charges des tickets s'effectuent depuis la vue "Organisation"

<p align="center">
<img src="/fr/img/affectationChargeTicket.png">
</p>

---

**Nos préconisations :**
<a id="analyseLogique"></a> 
>*Demandez aux responsables d'actions / tickets de renseigner la charge de réalisation. Cela permettra d'avoir une planification réaliste ainsi que de responsabiliser les acteurs à la réalisation du projet.* 

>*De plus vous donnerez l'opportunité de communiquer sur le réseau de réalisation du projet et ainsi faire des ajustements si nécessaire.*

>*Ne confondez pas la charge de réalisation et la durée de réalisation. Lors de la saisie de la charge de réalisation, ne prenez pas en compte les hypothèses de productivité. Ces hypothèses seront gérées au niveau du planning des collaborateurs*

---

## Etape 3 : Analyser le déroulement logique du projet

*Vue Weelgo : Logique*

La vue logique vous permet d'avoir une vision compléte de l'enchainement logique de réalisation de votre projet. Vous pouvez ainsi détécter des problèmes d'enchainements et/ou d'ordonnancement sur les actions / tickets.
<a id="hypoDepart"></a> 
__La génération du planning étant automatique__, il sera peut etre nécessaire de prioriser certaines actions. Pour cela, cliquer sur <img src="/fr/img/listePriorite.png"> afin d'indiquer la priorité. 

L'ordonnancement s'effectue de haut en bas. L'action la plus haute est plus prioritaire que l'action d'en dessous. 


## Etape 4 : Définition des hypothèses de départ

*Vue Weelgo : Date Wall*

Avant de vous lancez dans l'analyse du planning de votre projet, il est nécessaire de définir les hypothèses de départ. Elles sont au nombre de deux : 
* La date de début du projet


* La disponibilité des ressources. 



Sur weelgo les ressources sont, pour l'instant, uniquement des collaborateurs. La gestion des collaborateur s'effectue en gérant leur calendriers. 


( mettre image ) 

Vous pouvez définir sur cette vue : 
+ La date de début du projet
+ Le calendrier des collaborateurs

Ajoutez les calendriers de vos collaborateurs et definissez des dates spécifiques. Une fois la disponibilité renseignée, elle est automatiquement prise en compte dans la construction du planning du projet. 


---

**Nos préconisations :**

>*N'affectez pas vos collaborateurs à 100%. Prenez une marge, cela permettra d'avoir une gestion de projet plus souple et vous permettre d'absorber plus facilement les aléa de la vie du projet.*
<a id="analysePlanning"></a>
**Tips&Astuces :**
>*La modification du calendrier ou de la productivité générale de la personne impactera le planning depuis le début du projet. Afin de pas modifier le planning déjà réalisé, modifiez la charge à venir du collaborateur en ajoutant des dates spécifiques ( mettre image ).*

---


## Etape 5 : Analyser le planning et les indicateurs

Chez Weelgo, nous pensons que le manageur doit se concentrer sur l'essentiel. C'est à dire le management des hommes, la gestion des problèmes et des arbitrages. Le temps passé à généré des plannings et des indicateurs ne doit plus être à la charge du manageur. C'est pourquoi la solution Weelgo générère automatiquement l'ensemble des outils permettant de piloter le projet. 

### Le Wall

Véritable feuille de route du projet, c'est la vision verticale du planing. Vous pouvez identifier immédiatement les actions non planifiées ainsi que le déroulement du projet. 

<p align="center">
<img src="/fr/img/vueWall.png">
</p>


---

**Nos préconisations :**

>*Entre le vue Organisation et la vue Gantt, cette représentation est idéale pour le pilotage  de l'équipe au quotidien. Lors de la réunion journalière, en un clin d'oeil, l'ensemble de l'équipe connait les actions à réaliser ainsi que l'état du projet.* 

---


### Le Dashboard

Le Dashboard est le tableau de bord du projet. Cette vue permet d'avoir une vision 360 du projet et de l'ensemble des indicateurs cléfs: 
+ Les jalons
+ Le burdown 
+ Les problèmes

<p align="center">
<img src="/fr/img/dashboard1.png">
</p>


<p align="center">
<img src="/fr/img/dashboard2.png">
</p>

---

**Nos préconisations :**

>*Le tableau de bord est idéal dans la communication de l'avancement du projet. Notammement dans une relation client / fournisseur. Vous pouvez communiquer sur l'avancement des livrables-jalons cléfs du projet et de la santé du projet.*

---

### Le Gantt

Principal outil du pilotage de projet. Le gantt Weelgo regroupe les indicateurs nécessaires afin de prendre des décisions et des arbitrages. 

<p align="center">
<img src="/fr/img/gantt.png">
</p>


---
**Nos préconisations :**

>*Hesitez pas à afficher le calendrier de vos collaborateurs avant de modifier le réseau et / ou les tickets. La vision du calendrier dans le Gantt vous permet d'avoir la vision nécessaire sur la disponibilité de vos collaborateurs et donc vous permettre de modifier votre réseau en connaissance de cause.* 

---

### Le Burndown

Représentation graphique de l'évolution de la quantité de travail restantes par rapport au temps. 

<p align="center">
<img src="/fr/img/burndown.png">
</p>

---
**Nos préconisations :**

>*Attention, une consomation en dessous de la consommation idéal n'est pas forcement preuve de la bonne santé du projet. Seul l'avancement dans le gantt vous le garantira.* 

---


### Le droite à 45

Représentation graphique de l'évolution des dates de fin prévisionnelles des jalons du projet. La droite à 45° vous permet de savoir, en un coup d'oeil, l'évolution des différentes dates de livraison prévues. 

La droite à 45° est un puissant outil de détection des dérives et de reporting de projet. 

<p align="center">
<img src="/fr/img/droite45.png">
</p>

---
**Nos préconisations :**

>*Chaque livrable / jalon à sa propre droite à 45. Cette droite est accesible en cliquant sur le jalon depuis la vue dashboard.* 

( mettre image )

---

