---
layout : docs_fr
title : Gérez un projet Weelgo ! 
description : Dans ce tutoriel, vous apprendez les bonnes pratiques pour gérer correctement un projet Weelgo au quotidien
toc : true
---

## Introduction


Votre projet Weelgo est initialisé et vous devez maintenant piloter votre projet. Nous aborderons ce sujet au travers 3 axes : 
1. [L'importance du suivi du planning et des indicateurs](#importancePlanning)
2. [La mise à jour de l'avancement](#majAvancement)
2. [La gestion des imprévus](#gestionImprevus)
3. [Construire l'historique du projet](#historiqueProjet)


### Le management, quesako ?

Comment pouvons-nous définir le management ? Nous n'allons pas ici exposer ce sujet en détail. Néanmoins faisons ensemblre un bref rappel des composantes essentielles du management. 

**Manager, c'est composer avec 4 domaines :** 

+ L'organisation
+ L'animation, la communication et la motivation de l'équipe
+ Savoir faire-faire
+ Analyser, prévoir et décider 

Il est évident que le manageur ne peut pas être expert dans l'ensemble des domaines ci-dessus. Du fait de sa personnalité et de son expérience, un manageur peut avoir des facilités dans l'organisation et l'analyse et être moins efficace dans sa communication. 

Le manageur doit donc s'entourer d'une **équipe complémentaire** afin d'avoir des relais d'influences pour compenser certaines de ses faiblesses mais il doit aussi s'armer et utiliser des outils lui permettant d'accomplir sa mission. 

Cet outillage doit lui permettre de générer des indicateurs fiables et efficaces afin d'être efficient dans son rôle.  

Pour rappel, les principaux indicateurs que doit avoir le manageur sont : 

+ Le PERT
+ Le GANTT
+ Les Jalons 
+ La droite à 45
+ Le burndown
+ Le calendrier des ressources
<a id="importancePlanning"></a> 
Comme vous l'avez déjà vu, Weelgo met à votre disposition l'ensemble de ces indicateurs.

Etudions l'importance de la présence des indicateurs dans un projet et leur répercution sur l'ensemble des domaines évoqués ci-dessus. 

## 1.  L'importance du suivi du planning et des indicateurs

Une simple série de question permet d'estimer la bonne santé d'un projet  :  
+ Existe t-il un planning ? 
+ Le planning est-il à jour et partagé à l'ensemble de l'équipe ? 
+ Existe t'il des indicateurs d'avancements fiables ? Sont-il partagé à l'ensemble des collaborateurs ? 

Une réponses affirmative à l'ensemble de ces questions nous permet de savoir que le manageur a à sa disposition les moyens pour organiser, animer, communiquer, analyser, prévoir et décider. 

**Le planning doit être considéré comme l'élément cléf dans un projet.**


<p align="center">
<img src="/fr/img/planningDomaine.png">
</p>


C'est lui qui donne un **cadre de travail** à l'ensemble des intervenants dans le projet. C'est le fil d'ariane qui permet à tous les collaborateurs la possibilité de se situer dans un travail commun et dans une perspective globale. 

Il est donc vital d'avoir un planning mis à jour réguliérement. Cette gestion vivante du planning donne une impression de mouvement et de dynamisme au projet. 

Néanmoins, pour avoir une utilisation optimum du planning,  deux prérequis sont nécessaires  : 
1. **Faites participer vos équipes dans la planification.** Ce mode de gestion permettra la responsabilisation de votre équipe et augmentera sa motivation 
2. Le planning doit être à jour et accessible à chaque instant. 

**N'acceptez jamais de glissement de délai sans réagir**, même si les retards sont justifiés! Il faut toujours rechercher des solutions pour rattraper les retards et modifier le réseau du projet en conséquence. 
 
C’est la seule attitude qui peut sensibiliser les acteurs du projet à l’importance de la tenue des délais. **Une succession de glissements de délais enlève toute crédibilité au planning qui devient rapidement “lettre morte".** 

---

**Nos préconisations :**

>*Le planning à un sens uniquement si l'équipe lui en donne. Faites vivre le planning avec votre équipe*
<a id="majAvancement"></a> 
>*Partager le planning et les indicateurs. Ils doivent être accessible à chaque instant.* 

>*N'acceptez jamais un glissement de délai sans réagir. Trouvez des solutions et adapter votre réseau.* 

---

## 2. La mise à jour de l'avancement 

*Acteurs : Les responsables d'actions, Le chef de projet*


Comme nous venons de le voir, indiquer l'avancement du projet est important afin de piloter correctement. Dans l'outil weelgo, vous pouvez indiquer l'avancement depuis les vues : 
* La vue Réseau
* La vue Organisatin 
* La vue logique 

L'avancement se renseigne sur les actions et sur les tickets.

**Pour le suivi et la bonne santé du projet, il est nécessaire que l'avancement soit mis à jour par les responsables des actions ou le chef de projet.** 


**Pour les actions :**

En cliquant sur "En cours" et en définissant une progression depuis le bouton : <img src="/fr/img/boutonActualiser.png">

<p align="center">
<img src="/fr/img/actionMajAvancement.png">
</p>

**Pour les tickets :**

En cliquant sur l'icone suivante : 

<p align="center">
<img src="/fr/img/ticketMajAvancement1.png">
</p>

Puis indiquer l'avancement de la même manière que pour l'action

<p align="center">
<img src="/fr/img/ticketMajAvancement2.png">
</p>

### Le fonctionnement de l'avancement des actions et des tickets

Dans Weelgo, la mise à jour de l'avancement doit suivre la logique du réseau. Prenons l'exemple du réseau ci-dessous : 

<p align="center">
<img src="/fr/img/actionLienPhysique.png">
</p>

L'ordre de réalisation est l'action A ( et ses tickets ) puis ensuite l'action B ( et ses tickets ).  Lors du démarrage du projet, l'avancement du projet suivra cette logique. Si ce n'est pas le cas, c'est que le réseau ne correpondait pas à la réalité de réalisation. 

Par exemple, si vous essayez de commencer l'action B sans avoir terminée l'action A. Weelgo vous l'empechera en vous affichant le message suivant :

<p align="center">
<img src="/fr/img/impossibleStartAction.png">
</p>

Si vous devez quand même démarrer l'action B, c'est ce cette action n'attendait pas en input le livrable de l'action A. 

Le réseau aurait du être modélisé de la manière suivante : 

<img src="/fr/img/actionParallele.png">


Ou


<img src="/fr/img/actionLienTemporel.png">

Néanmoins, il y a certains cas ou nous pouvons quand même débuter l'action B avant l'action A. Par exemple, des activités préparatives à la réalisation de l'action B. Ces activités n'ont pas nécessairement besoin du livrable de l'action A mais ils peuvent être commencé. 

Cette gestion ne pose pas de problème dans l'outil Weelgo. Vous avez la possibilité : 
* D'indiquer un avancement sur les tickets, même si l'action n'est pas démarré. 

<p align="center">
<img src="/fr/img/majAvancementActionNonStart.png">
</p>

L'avancement d'une action est pris en compte par Weelgo quand l'action est démarrée. Vous pouvez indiquer un avancement sur le ticket, néanmoins il ne sera pas pris en compte tant que l'action est non démarée

* Démarrer l'action en utilisant les options de démarrage et de cloture des actions. 

### La gestion des options de démarrage / cloture des actions 

*Acteurs : Le chef de projet*

**Attention les options ci dessous sont à utiliser avec précaution. Il est obligatoire d'avoir l'autorisation du chef de projet avant de réaliser ce type d'opération.** 

<p align="center">
<img src="/fr/img/optionsAction.png">
</p>

Ces options permettent de court-circuiter le fonctionnement logique de déroulement du réseau. 
Les deux premières options permettent de démarrer ou terminer une action si les livrables de l'action ne sont pas présents. 

Néanmoins, si vous terminez une action sans les livrables nécessaires pour la réaliser cela indique que le livrable en input était pas nécessaire et donc un problème sur la conception de votre réseau. 

Lorsque vous démarrez ou terminez une action sans le livrable en input et meme si le livrable est déposé pendant la réalisation de l'action. Weelgo vous préviens que les livrables en input ne sont plus à jour. 

<p align="center">
<img src="/fr/img/livrableAmettreAjour.png">
</p>

Ceci est un comportement normal, cela indique que vous devez vérifier que le livrable fourni vous permet réelement de réaliser votre action. Si oui, vous devez rédémarrer l'action et indiquer le reste à faire suite à la récéption du livrable. 


---

**Nos préconisations :**

>*Mettez à jour l'avancement réguliérement.*
<a id="gestionImprevus"></a>
>*Vous êtes en présence d'un problème de conception du réseau si vous etes amenez à commencer / terminer des actions sans avoir réaliser les actions précédentes.*

>*Evitez au maximum d'utiliser les options permettant de forcer le démarrage / cloture d'une action.*

>*Faites saisir l'avancement par les responsables des actions.*

---

## 3. La gestion des imprévus

*Acteurs : Le chef de projet*

**Comme nous allons le voir, une modification du réseau sera nécessaire pour gérer les imprevus. Toutes modifications du réseau doit être réaliser par le chef de projet uniquement.** 

Lors de la réalisation de votre projet, vous allez avoir à gérer des imprévus. C'est la gestion des imprévus qui rend complexe la réalisation d'un projet. 

En effet, ces imprévus vont avoir des conséquences sur la planification, les couts, la gestion humaines de votre projet et sur votre relation client / fournisseur.  

A défaut de pouvoir les anticiper, il faut pouvoir les gérer correctements. Une bonne gestion des imprévus est la capacité à pouvoir les intégrer dans le planning de réalisation, en voir les conséquences et ainsi adapter le déroulement du projet en fonction. 

Deux types d'imprévus possibles. les imprévus liées directement au projet. Et les imprévus, non liés au projet mais l'affectant directement. Des actions différents sont alors possible sous Weelgo pour prendre en compte ces deux types d'imprévus. 


### Les imprévus liés au projet

Les imprévus liées au projet sont généralement : 
+ Un retard dans la réalisation d'une action 
+ L'oubli d'une action dans la réalisation du réseau 
+ Une activités qui vient se greffer au projet. 

Ces imprévus ont toutes la même caractéristique. Ils impactent le réseau, une action ou un ticket. C'est donc sur ces éléments que nous devons intervenir pour gérer l'imprévu. 

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
+ Soit il a été mal estimé au niveau de la charge de réalisation. Dans se cas, il faut agmenter la charge de réalisation de l'action/ticket
+ Soit c'est la durée de réalisation qui a été mal estimée. Il faut forcer la durée de réalisation de l'action/ticket pour qu'elle corresponde à la réalité. 

Une action estimé à 4 jh en moyenne peut être réalisé en 2 j de travail par une personne plus expérimenté. Généralement dans ce cas, nous préconisons d'indiquer la charge en fonction de la personne qui traite l'activité. 


#### L'oubli d'une action / une activité venant se greffer au projet

Si une activité doit etre rajouter dans le projet, vous devez déjà identifié son type : Action ou ticket. 

Si c'est une activité nécessitant un livrable supplémentaire au projet, elle doit être gérée en créant une action dans le réseau. Sinon il suffira de créer un ticket dans la vue organisation. 

### Les imprévus non liés au projet

Si l'imprévu n'est pas lié au projet, cela veut dire qu'un de vos collaborateurs ne pourra pas travailler pour votre projet autant que prévu initialement. 

La modification doit alors s'effectué au niveau du calendrier de la ressource. 

<p align="center">
<img src="/fr/img/ajoutDateSpecifique.png">
</p>

Vous devez indiquer que le collaborateur ne travaillera pas ( ou moins ) durant la période de réalisation de l'imprévu. 


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

Nous avons déjà évoqué l'utilsiation de la durée pour gérer un retard. Les dates de début et date de fin s'utilisent dans 2 cas : 
1. Pour situer le démarrage d'une action dans le temps. Par exemple, une action situé en début de réseau, précédé par aucune action mais nécessitant de commencer plus tard dans le temps ( et non à la date de démarrage du projet ).

<p align="center">
<img src="/fr/img/actionDebutReseau.png">
</p>

2.  __recadrer__ le projet dans le temps suite à un retard ou un imprévus non géré correctement ( notamment par un manque de suivi )


Forcer une date permet donc de resituer le démarrage ( ou la fin ) d'une action et d'un ticket dans le temps. Vous devez limiter au maximum l'utilisation de cette option. 

De plus, Weelgo ne court-circuite pas les charges indiqués sur les actions quand vous renseignez une date. Si les charges du réseau indique une date de fin de l'action au 19/10/2017. SI vous indiquer une date de fin de l'action au 08/12/2017, le planning indiquera une erreur. 

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

>*Les modifications du réseau doivent être réaliser par le responsable du réseau*

>*Limitez l'utilisation des dates de début et des dates de fin.*

>*Le recadrage du planning s'effectue uniquement si les charges du réseau le permettent !*

---

### Analyse et arbitrage. 

Vous venez d'effectuer les modifications nécessaires afin d'intégrer l'imprévu dans votre réseau. Vous pouvez alors analysez les impacts sur votre planification et notamement au niveau des jalons clef. Il y a de fortes chances que les dates des jalons clefs ont été modifiées. 

Deux possibilités s'offre à vous : 
1. Les nouvelles dates vous conviennent et vous n'avez donc rien à faire de plus.
2. Elles ne vont conviennent pas et vous devez donc retravailler votre réseau / organisation afin d'aboutir au résultat voulu.

<a id="historiqueProjet"></a>

La modification du réseau doit être effectué par le responsable du réseau. 
Cet arbitrage peut avoir été partagé avec l'équipe mais toute modification du réseau reste à la charge du responsable. 
 
## 4. Construire l'historique du projet

Dans weelgo, vous avez la possibilité de construire l'historique du projet. Cet historique ou snapshot, permet de prendre une photo du projet à un instant T. 

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






