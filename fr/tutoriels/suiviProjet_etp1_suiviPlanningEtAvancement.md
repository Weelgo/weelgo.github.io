---
layout : docs_fr
title : Gérez un projet Weelgo ! 
description : 
toc : true
group : followUp
id : fzt356
readingEstimation : 4
---


## Introduction
---

Votre projet Weelgo est initialisé et vous devez maintenant le piloter. Nous aborderons ce sujet au travers 3 axes : 
+L'importance du suivi du planning et des indicateurs
+La mise à jour de l'avancement

---

### Rappel : Qui fait quoi dans Weelgo?

Avant de débuter ce tutoriel, faisons un bref rappel de qui doit faire quoi dans Weelgo.

Dans Weelgo, les rôles sont simples. Nous avons : 
* Le chef de projet. C'est généralement le responsable du réseau.
* Les exécutants des actions / tickets : Ce sont les personnes reponsables des actions et des tickets. Ils sont désignés par le chef de projet. 

Ci-dessous la matrice des rôles que nous vous conseillons: 

**Le responsable du réseau / chef de projet :** 
+ Il créer la structure et l'organisation du projet
+ Il modifie le réseau, sa strcuture ainsi que les charges de réalisation 

**Le responsable d'action :** 
+ Il indique l'avancement et le reste à faire sur ses actions / tickets

---


### Le management, quesako ?

Comment pouvons-nous définir le management ? Nous n'allons pas ici exposer ce sujet en détail, néanmoins faisons ensemble un bref rappel des composantes essentielles du management. 

**Manager, c'est composer avec 4 domaines :** 

+ L'organisation
+ L'animation, la communication et la motivation de l'équipe
+ Le savoir faire-faire
+ Analyser, prévoir et décider 

Il est évident que le manageur ne peut pas être expert dans l'ensemble des domaines ci-dessus. Du fait de sa personnalité et de son expérience, un manageur peut avoir des facilités dans l'organisation et l'analyse mais être moins efficace dans sa communication. 

Le manageur doit donc s'entourer d'une **équipe complémentaire** afin d'avoir des relais d'influences pour compenser certaines de ses faiblesses mais il doit aussi s'armer et utiliser des outils lui permettant d'accomplir sa mission. 

Cet outillage doit lui permettre de générer des indicateurs fiables et efficaces afin d'être efficient dans son rôle.  

Pour rappel, les principaux indicateurs que doit avoir le manageur sont : 

+ Le PERT
+ Le GANTT
+ Les jalons 
+ La droite à 45°
+ Le burndown
+ Le calendrier des ressources
<a id="importancePlanning"></a> 


Vous le savez déjà, Weelgo met à votre disposition l'ensemble de ces indicateurs.

Etudions donc l'importance de la présence des indicateurs dans un projet et leur répercution sur l'ensemble des domaines évoqués ci-dessus. 

## L'importance du suivi du planning et des indicateurs
---


Une simple série de question permet d'estimer la bonne santé d'un projet  :  
+ Existe t-il un planning ? 
+ Le planning est-il à jour et partagé à l'ensemble de l'équipe ? 
+ Existe t'il des indicateurs d'avancement fiables ? Sont-il partagés à l'ensemble des collaborateurs ? 

Une réponses affirmative à l'ensemble de ces questions nous permet de savoir que le manageur a à sa disposition les moyens pour organiser, animer, communiquer, analyser, prévoir et décider. 

**Le planning doit être considéré comme l'élément cléf dans un projet.**


<p align="center">
<img src="/fr/img/planningDomaine.png">
</p>


C'est lui qui donne un **cadre de travail** à l'ensemble des intervenants dans le projet. C'est le fil d'ariane qui permet à tous les collaborateurs d'avoir la possibilité de se situer dans un travail commun et dans une **perspective globale**. 

Il est donc vital d'avoir un planning mis à jour régulièrement. Cette gestion vivante du planning donne une impression de **mouvement et de dynamisme** au projet. 

Néanmoins, pour avoir une utilisation optimum du planning, deux prérequis sont nécessaires  : 
1. **Faites participer vos équipes dans la planification.** Ce mode de gestion permettra la responsabilisation de votre équipe et augmentera sa motivation 
2. **Le planning doit être à jour et accessible à chaque instant.** 

**N'acceptez jamais de glissement de délai sans réagir**, même si les retards sont justifiés! Il faut toujours rechercher des solutions pour rattraper les retards et modifier le réseau du projet en conséquence. 
 
C’est la seule attitude qui peut sensibiliser les acteurs du projet à l’importance de la tenue des délais.

**Une succession de glissements de délais enlève toute crédibilité au planning qui devient rapidement “lettre morte".** 

---

**Nos préconisations :**

>*Le planning à un sens uniquement si l'équipe lui en donne.*

>*Faites vivre le planning avec votre équipe*
<a id="majAvancement"></a> 

>*Partager le planning et les indicateurs. Ils doivent être accessibles à chaque instant.* 

>*N'acceptez jamais un glissement de délai sans réagir. Trouvez des solutions et adapter votre réseau.* 

---

## La mise à jour de l'avancement 
---


*Acteurs : Les responsables d'actions, Le chef de projet.*


Comme nous venons de le voir, indiquer l'avancement du projet est important afin de piloter correctement. Dans l'outil Weelgo, vous pouvez indiquer l'avancement depuis les vues : 
* La vue Réseau
* La vue Organisation 
* La vue Logique 

L'avancement se renseigne sur les actions et sur les tickets.

**Pour le suivi et la bonne santé du projet, il est nécessaire que l'avancement soit mis à jour par les responsables des actions ou le chef de projet.** 


**Pour les actions :**

En cliquant sur "En cours" et en définissant une progression depuis le bouton : <img src="/fr/img/boutonActualiser.png">

<p align="center">
<img src="/fr/img/actionMajAvancement.png">
</p>

**Pour les tickets :**

En cliquant sur l'icone suivante : <img src="/fr/img/ticketMajAvancement1.png">

Puis indiquer l'avancement de la même manière que pour l'action

<p align="center">
<img src="/fr/img/ticketMajAvancement2.png">
</p>

### Le fonctionnement de l'avancement des actions et des tickets

Dans Weelgo, la mise à jour de l'avancement doit **suivre la logique du réseau**. 

Prenons l'exemple du réseau ci-dessous : 

<img src="/fr/img/actionLienPhysique.png">


L'ordre de réalisation est l'action A (et ses tickets) puis ensuite l'action B (et ses tickets).  

Si vous essayez de commencer l'action B sans avoir terminée l'action A, Weelgo vous l'empechera en vous affichant le message suivant :

<p align="center">
<img src="/fr/img/impossibleStartAction.png">
</p>

Si vous devez quand même démarrer l'action B, c'est que cette action n'attendait pas en input le livrable de l'action A et donc que votre réseau ne correspondait pas à la réalité de réalisation. Cela permet de mettre en évidence des problèmes de conception. 

Le réseau aurait du être modélisé de la manière suivante : 

<p align="center">
<img src="/fr/img/actionParallele.png">
Ou        
<img src="/fr/img/actionLienTemporel.png">
</p>


** Les cas particuliers **

Néanmoins, il y a certains cas où nous pouvons quand même débuter l'action B avant l'action A. 

Par exemple, s'il existe des activités permettant de préparer la réalisation de l'action B, ces activités n'ont pas nécessairement besoin du livrable de l'action A, mais elles peuvent être commencées. 

Dans ce cas, vous avez la possibilité : 
* D'indiquer un avancement sur les tickets, même si l'action n'est pas démarrée. 

<p align="center">
<img src="/fr/img/majAvancementActionNonStart.png">
</p>

Vous pouvez indiquer un avancement sur le ticket, néanmoins il ne sera pas pris en compte tant que l'action est non démarrée

* Démarrer l'action en utilisant les options de démarrage et de clôture des actions. 

### La gestion des options de démarrage / clôture des actions 

*Acteur : Le chef de projet*

**Attention les options ci-dessous sont à utiliser avec précaution. Il est obligatoire d'avoir l'autorisation du chef de projet avant de réaliser ce type d'opération.** 

<p align="center">
<img src="/fr/img/optionsAction.png">
</p>

Ces options permettent de **court-circuiter le fonctionnement logique** de réalisation du réseau. 

Les deux premières options permettent de démarrer ou terminer une action si les livrables de l'action ne sont pas présents. 

Si vous terminez une action sans avoir les inputs, c'est qu'ils n'étaient pas nécessaires. Il existe donc un problème de conception du réseau.

Lorsque vous démarrez ou terminez une action sans le livrable en input, lorsque l'action réceptionne finalement son input, Weelgo vous préviens que les livrables en entrée ne sont plus à jour. 

<p align="center">
<img src="/fr/img/livrableAmettreAjour.png">
</p>

**Ceci est un comportement normal**, cela indique que vous devez vérifier que le livrable fournis vous permet réellement de réaliser votre action. Vous devez donc rédémarrer l'action et indiquer le reste à faire suite à la récéption du livrable. 


---

**Nos préconisations :**

>*Mettez à jour l'avancement réguliérement.*
<a id="gestionImprevus"></a>
>*Vous êtes en présence d'un problème de conception du réseau si vous êtes amenez à commencer / terminer des actions sans avoir réaliser les actions précédentes.*

>*Evitez au maximum d'utiliser les options permettant de forcer le démarrage / clôture d'une action.*

>*Faites saisir l'avancement par les responsables des actions.*

>*Si vous effectuez des actions non autorisées par nature par Weelgo c'est que vous avez des problèmes de conception au niveau du réseau."
