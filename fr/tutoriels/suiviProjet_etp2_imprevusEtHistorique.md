---
layout : docs_fr
title : Gérez un projet Weelgo ! 
description : 
toc : true
group : followUp
id : oknr847
readingEstimation : 4
---

## Introduction
---

Votre projet Weelgo est en cours de réalisation. Vous aller devoir gérer des imprévus ainsi que commencer à construire l'historique du projet pour pouvoir suivre son déroulement.
1. [La gestion des imprévus](#gestionImprevus)
2. [La construction de l'historique du projet](#historiqueProjet)


## 1. La gestion des imprévus
---


*Acteur : Le chef de projet*

**Comme nous allons le voir, une modification du réseau sera nécessaire pour gérer les imprévus. Toute modification du réseau doit être réalisée par le chef de projet uniquement.** 

Lors de la réalisation de votre projet, vous allez avoir à gérer des imprévus. C'est la gestion des imprévus qui rend complexe la réalisation d'un projet. 

En effet, ces imprévus vont avoir des conséquences sur la planification, les coûts, la gestion humaine de votre projet et sur votre relation client / fournisseur.  

A défaut de pouvoir les anticiper, il faut pouvoir les gérer correctement. Une bonne gestion des imprévus est la capacité à pouvoir les intégrer dans le planning de réalisation, en voir les conséquences et ainsi adapter le déroulement du projet en fonction. 

Deux types d'imprévus possibles: les imprévus liés directement au projet, et les imprévus non liés au projet mais l'affectant directement. Des actions différentes sont alors possibles sous Weelgo pour prendre en compte ces deux types d'imprévus. 


### Les imprévus liés au projet

Les imprévus liés au projet sont généralement : 
+ Un retard dans la réalisation d'une action 
+ L'oubli d'une action dans la réalisation du réseau 
+ Une activité qui vient se greffer au projet. 

Ces imprévus ont toutes la même caractéristique. Ils impactent le réseau, une action ou un ticket. C'est donc sur ces éléments que nous devons intervenir. 

#### Un retard sur une action/ticket

Dans Weelgo, si le reste à faire est saisi réguliérement, le retard sur une action / ticket est détéctable immédiatement. 

**Vue Date Wall :** 

<p align="center">
<img src="/fr/img/projetRetadDateWall.png">
</p>


**Vue dashboard :** 

<p align="center">
<img src="/fr/img/projetRetadDashboard.png">
</p>

Si ce retard est irrattrapable, il peut être de deux sortes : 
+ Soit il a été mal estimé au niveau de la charge de réalisation. Dans se cas, il faut augmenter la charge de réalisation de l'action/ticket

<p align="center">
<img src="/fr/img/ticketModifierCharge.png">
</p>

+ Soit c'est la durée de réalisation qui a été mal estimée. Il faut forcer la durée de réalisation de l'action / ticket pour qu'elle corresponde à la réalité. 

<p align="center">
<img src="/fr/img/ticketModifierDuree.png">
</p>

Une action estimée à 4 jh en moyenne peut être réalisée en 2 j de travail par une personne plus expérimentée. Nous préconisons d'indiquer la charge en fonction de la personne qui traite l'activité. 


#### L'oubli d'une action / une activité venant se greffer au projet

Si une activité doit être rajouter dans le projet, vous devez déjà identifié son type : Action ou ticket. 

Si c'est une activité nécessitant un livrable supplémentaire au projet, elle doit être gérée en créant une action dans le réseau. Sinon il suffira de créer un ticket dans la vue organisation. 

### Les imprévus non liés au projet

Si l'imprévu n'est pas lié au projet, cela veut dire qu'un de vos collaborateurs ne pourra pas travailler pour votre projet autant que prévu initialement. 

La modification doit alors s'effectuer au niveau du calendrier de la ressource. 

<p align="center">
<img src="/fr/img/ajoutDateSpecifique.png">
</p>

Vous devez indiquer que le collaborateur ne travaillera pas (ou moins) durant la période de réalisation de l'imprévu. 


<p align="center">
<img src="/fr/img/calendrierRessource.png">
</p>

### L'utilisation des dates de début et date de fin 

Sur les actions et les tickets, vous avez la possibilité de forcer :
+ Une durée
+ Une date de début
+ Une date de fin 

<p align="center">
<img src="/fr/img/forcerDateAction.png">
</p>

Nous avons déjà évoqué l'utilisation de la durée pour gérer un retard. Les dates de début et dates de fin s'utilisent dans 2 cas : 
1. Pour situer le démarrage d'une action dans le temps. Par exemple, une action située en début de réseau, précédée par aucune action mais nécessitant de commencer plus tard dans le temps (et non à la date de démarrage du projet).

<p align="center">
<img src="/fr/img/actionDebutReseau.png">
</p>

2.  __Recadrer__ le projet dans le temps suite à un retard ou un imprévu non géré correctement ( notamment par un manque de suivi )


Forcer une date permet donc de resituer le démarrage ( ou la fin ) d'une action et d'un ticket dans le temps. Vous devez limiter au maximum l'utilisation de cette option. 

De plus, **Weelgo ne court-circuite pas les charges indiquées sur les actions** quand vous renseignez une date.

Si les charges du réseau indiquent une date de fin de l'action au 19/10/2017 et que vous indiquez une date de fin de l'action au 08/12/2017, le planning indiquera une erreur. 

**Ajout de la date de fin sur l'action :** 

<p align="center">
<img src="/fr/img/forcerDateFinAction.png">
</p>


**Le résultat sur le GANTT :**

<p align="center">
<img src="/fr/img/forcerDateFinProblemeGantt.png">
</p>

Pour ne pas avoir de message d'erreur dans le GANTT. il faut que la date de fin que vous indiquez soit positionnée après la date de fin calculée par le réseau ( donc apres le 19/10/2017 ).


<p align="center">
<img src="/fr/img/forcerDateFinActionOK.png">
</p>

**Le résultat sur le GANTT :**

<p align="center">
<img src="/fr/img/forcerDateFinGanttOK.png">
</p>

---

**Nos préconisations :**
<a id="ordreActions"></a> 

>*Les modifications du réseau doivent être réalisées par le responsable du réseau*

>*Limitez l'utilisation des dates de début et des dates de fin.*

>*Le recadrage du planning s'effectue uniquement si les charges du réseau le permettent !*

---

### Analyse et arbitrage. 

Vous venez d'effectuer les modifications nécessaires afin d'intégrer l'imprévu dans votre réseau. Vous pouvez alors analysez les impacts sur votre planification et notamement au niveau des jalons clés. Il y a de fortes chances que les dates des jalons clés aient été modifiées. 

Deux possibilités s'offrent à vous : 
1. Les nouvelles dates vous conviennent et vous n'avez donc rien à faire de plus.
<a id="historiqueProjet"></a>
2. Elles ne vont conviennent pas et vous devez donc retravailler votre réseau / organisation afin d'aboutir au résultat voulu.


**La modification du réseau doit être effectué par le responsable du réseau.**

Cet arbitrage peut avoir été partagé avec l'équipe mais toute modification du réseau reste à la charge du responsable. 
 
## 2. La construction de l'historique du projet
---


Dans Weelgo, vous avez la possibilité de construire l'historique du projet. Cet historique ou snapshot, permet de prendre une photo du projet. 

Afin de pouvoir consolider l'avancement du projet dans le gantt, burdnow et droit à 45°, vous devez effectuer un snapshot régulérement. 

<p align="center">
<img src="/fr/img/historiquePrendreSnap.png">
</p>

En plus de pouvoir consolider l'avancement, vous aurez à votre disposition le déroulement du projet. 

**Avancement du projet dans le burdown :**


<p align="center">
<img src="/fr/img/historiqueBurndown.png">
</p>

**Mise à jour de la droite à 45 :**


<p align="center">
<img src="/fr/img/droite45.png">
</p>


**Météo général du projet :**


<p align="center">
<img src="/fr/img/historiqueSnap.png">
</p>


Lors de la génération d'un snapshot, vous pouvez renseigner la météo du projet ainsi que rajouter des commentaires. 

<p align="center">
<img src="/fr/img/historiqueMeteoProjet.png">
</p>

Si vous gérez plusieurs projets en même temps, cela vous aidera dans votre présentation du projet à un tiers. 

---

**Nos préconisations :**

>*Faites des snapshots réguliérement afin de construire l'historique du projet*

>*Renseignez la météo du projet et ajoutez des commentaires*

---
