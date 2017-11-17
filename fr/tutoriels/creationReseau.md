---
layout : docs_fr
title : Créer et gérer un projet sous Weelgo
description : Dans ce tutoriel, vous apprendrez à créer et gérer un projet Weelgo au quotidien.
toc : true
---


## Etape 1 : Modéliser son projet. 

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

( Mettre image ici ) 

Ces répertoires contiendront les différentes actions nécessaire à la réalisation de votre projet. 

---
**Nos préconisations :**

>Effectuez des découpages simples. Au plus proche de la réalité. Des découpages complexes peuvent compliquer la gestion de votre projet 

---


### Les actions

Suite à la création de la structure du projet. Il est nécessaire de déterminer l'ensemble des actions qui devront être réalisées. 

Dans Weelgo, chaque action doit aboutir à un livrable. Une action ne peut pas être sans livrable !

Pour chaque action, il est nécessaire de se poser les questions suivantes :
* Que dois-je faire pour réaliser cette action? 
* Quel sont les inputs nécessaires à la réalisation de cette action? 
* Qu'ai-je en sortie de mon action ? 

Gardez en mémoire que vous avez la possibilité de saisir des tickets dans actions ( depuis la vue Organisation ). Un choix peut structurel sympose donc. Dois-je créer une action ou un ticket? 

Pour vous aidez dans votre choix, dites-vous que le réseau doit matérialiser la structure de votre projet. Notamment avec la liste des livrables de votre projet. Si le résultat du ticket et un livrable de haute importante ( application, documentation... ), une action est préférable. Dans le cas contraire, privilégiez le ticket.

Nous vous conseillons donc de construire vos actions en fonction des livrables qui doivent être livrés. 

---
**Nos préconisations :**

>Le réseau doit être structuré par des actions fournissant des livrables clés. Une action n'aboutissant pas à un livrable de haute importance doit plutot être traitée comme un ticket ( depuis la vue Organisation )

---


### L'ordonnancement des actions


L'ordonnancement  permet de mettre en ordre l'ensemble des actions. Nous déterminons ainsi les dépendances entre chaque tâches et leur chronologie. La solution Weelgo propose 2 type d'ordonnancement. L'ordonnancement "physique" et l'ordonnancement "temporel". 

L'ordonnancement "physique" est le lien entre 2 actions reliées par un livrable. L'action B attendant le livrable de l'action A afin de commencer 

( mettre image )

L'ordonnancement "temporel" correspond à une dépendance temporelle entre 2 actions. L'action B ne pouvant commencer uniquement quand l'action A est terminée. Néanmoins, le livrable de l'action A n'est pas nécessaire à la réalisation de l'action B

( mettre image )

Durant cette étape, il est nécessaire de considérer les ressources comme infinies. Cela permettra de connaitre le délai minimum possible avec le maximum de parallélisme )

---
**Nos préconisations :**

>Ordonnancez votre projet sans prendre en compte les ressources ( ressources infinie ). Vous connnaitrez le délai minimum de réalisation de votre projet et vous pourrez déterminer le nombre maximum de personne pouvant être affecté sur votre projet sur les différentes phases. 

---

## Etape 2 : L'organisation opérationnel du projet. 


## Création des tickets

**Nos préconisations :**

> TODO

---

## Affectation des ressources


**Nos préconisations :**

> TODO

---


## Renseignez des charges de réalisation

**Nos préconisations :**

> TODO

---



