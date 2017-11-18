---
layout : docs_fr
title : Créer et gérer un projet sous Weelgo
description : Dans ce tutoriel, vous apprendrez à créer et gérer un projet Weelgo au quotidien.
toc : true
---


## Etape 1 : Modéliser son projet. 


*Vue Weelgo : Réseau*

### La structure 

La solution Weelgo permet de modéliser son projet au travers un réseau d'actions / livrables. Une identification de la structure du réseau est donc nécessaire. Cette structuration s'effectue au travers la détermination de l'ensemble des phases permettant de réaliser votre projet

Ce découpage permettra de faciliter la compréhension et sa gestion au quotidien. 

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

Suite à l'identification des phases de votre projet, vous pouvez créer la structure du projet dans Weelgo. Cela est matérialisé par la création de répertoires et de sous répertoires dans la vue "Réseau"

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

---
**Nos préconisations :**

>Effectuez des découpages simples. Au plus proche de la réalité. Des découpages complexes peuvent compliquer la gestion de votre projet 

---


### Les actions

Suite à la création de la structure du projet. Il est nécessaire de déterminer l'ensemble des actions qui devront être réalisées. 

Dans Weelgo, chaque action doit aboutir à un livrable. Une action ne peut pas être sans livrable !

Ces livrables peuvent être de 3 types. Des livrables neutres, intermédiaire ou des jalons. 

<p align="center">
<img src="/fr/img/actions.png">
</p>

Pour chaque action, il est nécessaire de se poser les questions suivantes :
* Que dois-je faire pour réaliser cette action? 
* Quel sont les inputs nécessaires à la réalisation de cette action? 
* Qu'ai-je en sortie de mon action ? 

Gardez en mémoire que vous avez la possibilité de saisir des tickets dans actions ( depuis la vue Organisation ). Un choix peut structurel sympose donc. Dois-je créer une action ou un ticket? 

Pour vous aidez dans votre choix, dites-vous que le réseau doit matérialiser la structure de votre projet. Notamment avec la liste des livrables de votre projet. Si le résultat du ticket et un livrable de haute importante ( application, documentation... ), une action est préférable. Dans le cas contraire, privilégiez le ticket.

Nous vous conseillons donc de construire vos actions en fonction des livrables qui doivent être livrés. 

Dans weelgo, chaque action doit obligatoirement avoir des livrables. 

---
**Nos préconisations :**

>Le réseau doit être structuré par des actions fournissant des livrables clés. Une action n'aboutissant pas à un livrable de haute importance doit plutot être traitée comme un ticket ( depuis la vue Organisation )

---


### L'ordonnancement des actions


L'ordonnancement  permet de mettre en ordre l'ensemble des actions. Nous déterminons ainsi les dépendances entre chaque action et leur chronologie. La solution Weelgo propose 2 type d'ordonnancement. L'ordonnancement "physique" et l'ordonnancement "temporel". 

L'ordonnancement "physique" est le lien entre 2 actions reliées par un livrable. L'action B attendant le livrable de l'action A afin de commencer 

( mettre image )

L'ordonnancement "temporel" correspond à une dépendance temporelle entre 2 actions. L'action B ne pouvant commencer uniquement quand l'action A est terminée. Néanmoins, le livrable de l'action A n'est pas nécessaire à la réalisation de l'action B

( mettre image )

Dans weelgo la définition des actions et l'ordonnancement s'effectue en même temps. En effet, cette étape se traduit par la réalisation d'un réseau d'action.

Durant cette étape, il est nécessaire de considérer les ressources comme infinies. Cela permettra de connaitre le délai minimum possible avec le maximum de parallélisme )

( mettre image )

---
**Nos préconisations :**

>Ordonnancez votre projet sans prendre en compte les ressources ( ressources infinie ). Vous connnaitrez le délai minimum de réalisation de votre projet et vous pourrez déterminer le nombre maximum de personne pouvant être affecté sur votre projet sur les différentes phases. 

---

## Etape 2 : L'organisation opérationnel du projet. 

*Vue Weelgo : Organisation*

La vue Organisation de Weelgo représente le projet sous une forme hierachique ou WBS ( Work Breakdown Structure ). C'est à dire un organigramme des actions du projet. 

Cet organigramme est construit de la manière suivante : 
+ Les répertoires correspondent aux différents niveaux du WBS
+ Les actions correspondent au niveau le plus bas. 

( mettre image )

Vous allez donc pouvoir finaliser l'organisation de votre projet en ajoutant :
+ Les tickets associés aux actions
+ Ajouter des responsables
+ Ajouter des charges de réalisation 

### Création des tickets

Dans Weelgo, les tickets sont obligatoirement rattachés à une action. Les tickets doivent être considérés comme une décomposition plus fine de l'action. 

Ils peuvent être créés en cliquant sur ( mettre image ). Ils peuvent être déplacé ( via du drag&drop ) dans la liste des tickets ou dans d'autres actions. 

Le livrable etant rattaché à l'action, les tickets n'aboutissent pas à un livrable dans Weelgo. Néanmoins, ils ont des caractéristiques communes. Vous pouvez affectez des responsables aux tickets ainsi que des charges de réalisation. 

Les tickets sont priorisés de haut en bas. Les tickets situés le plus en haut sont plus prioritaires que les tickets en dessous ( mettre image )
 
---
**Nos préconisations :**

> Considérer les tickets comme la TODO liste de l'action. 

**Tips&Astuces :**
> Un ticket sans charge de réalisation peut être géré comme un ticket avec une charge. Néanmoins il apparaitra pas dans les vues de planification. 

---

### Affectation des responsables

L'affectation des responsables permet de transmette la responsabilité de l'action à un collaborateur. 

Pour cela, trouvez votre collaborateur depuis le bouton Ressources ( mettre image ) et cherchez le depuis la recherche ( mettre image ). 

Une fois séléctionné, il suffit d'affecter ( drag&drop ) la personne à une action ou à un ticket. ( mettre image )

---
**Nos préconisations :**
> Affectez un responsable unique à une action 

**Tips&Astuces :**
> Si l'action contient plusieurs responsable. Nous considérons que l'action sera réalisée par l'ensemble des collaborateurs en même temps ( en fonction de leurs disponibilités ). La charge de réalisation sera alors distribuée entre tous les responsables. 

---
### Renseignez des charges de réalisation

La charge de réalisation correspond au temps nécessaire afin de réaliser l'action. Une action / ticket ne peut être plannifié uniquement si il une charge de réalisation est présente. 

L'affectation des charges des actions s'effectuent depuis la vue "Réseau" 

( mettre image )

L'affectation des charges des tickets s'effectuent depuis la vue "Organisation"

( mettre image )

---
**Nos préconisations :**

> Demandez aux responsables d'actions / tickets de renseigner la charge de réalisation. Cela permettra d'avoir une planification réaliste ainsi que de responsabiliser les acteurs à la réalisation du projet. 

> De plus vous donnerez l'opportunité de communiquer sur le réseau de réalisation du projet et ainsi faire des ajustements si nécessaire

---

## Etape 2 : Analyser le déroulement logique du projet

*Vue Weelgo : Logique*

La vue logique vous permet d'avoir une vision compléte de l'enchainement logique de réalisation de votre projet. Vous pouvez ainsi détécter des problèmes d'enchainements et/ou d'ordonnancement sur les actions / tickets.

La génération du planning étant automatique, il sera peut etre nécessaire de prioriser certaines actions. Pour cela, cliquer sur ( mettre image ) afin d'indiquer la priorité. 

L'ordonnancement s'effectue de haut en bas. L'action la plus haute est plus prioritaire que l'action d'en dessous. 


## Etape 3 : Date de début du projet et disponibilité des ressources

*Vue Weelgo : Date Wall*

Sur weelgo les ressources sont, pour l'instant, uniquement des collaborateurs. La gestion des collaborateur s'effectue en gérant leur calendriers. 

https://github.com/Weelgo/weelgo.github.io/blob/master/fr/img/unnamed.png?raw=true

( mettre image ) 

Vous pouvez définir sur cette vue : 
+ La date de début du projet
+ Le calendrier des collaborateurs

Ajoutez les calendriers de vos collaborateurs et definissez des dates spécifiques. Une fois la disponibilité renseignée, elle est automatiquement pris en compte dans la construction du planning du projet. 


---
**Nos préconisations :**

> N'affectez pas vos collaborateurs à 100%. Prenez une marge, cela permettra d'avoir une gestion de projet plus souple et vous permettre d'absorber plus facilement les aléa de la vie du projet

**Tips&Astuces :**
> La modification du calendrier ou de la productivité générale de la personne impactera le planning depuis le début du projet. Afin de pas modifier le planning déjà réalisé, modifiez la charge à venir du collaborateur en ajoutant des dates spécifiques ( mettre image )

---

## Etape 4 : Analyser le planning et les indicateurs

### Le Wall

### Le Dashboard

### Le Gantt

### Le Burndown
