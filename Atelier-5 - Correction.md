# Atelier 5 – Du plan au backlog (50 min, en groupes)

Nous sommes au début de la séquence S3. L'équipe Scrum prépare la fonctionnalité **« Ouverture e-mail par IA – cas nominal »**.

Ce que l'on sait :

- Les OM arrivent sur une boîte e-mail partagée, mélangés à d'autres messages (relances, questions, publicités).
- L'OM est en pièce jointe, au format PDF. Chaque compagnie a sa mise en page.
- Le service d'IA de NeoDoc reçoit un PDF et renvoie les champs extraits, chacun avec un score de confiance de 0 à 100.
- L'API d'ouverture livrée en S1 sait créer un dossier à partir de données structurées.
- Un gestionnaire doit pouvoir reprendre la main quand l'IA n'est pas sûre d'elle.
- Les e-mails contiennent des données personnelles.
- L'équipe livre en moyenne **24 points par sprint** de deux semaines.

Exemple de user story rédigée :

> **En tant que** gestionnaire du plateau d'ouverture,
> **je veux** que les données de l'ordre de mission soient extraites automatiquement du PDF,
> **afin de** ne plus les ressaisir.
>
> Critères d'acceptation :
> - Étant donné un PDF d'OM de la compagnie pilote, quand il est soumis à l'extraction, alors les champs compagnie, numéro de sinistre, nom de l'assuré, adresse du sinistre et nature du sinistre sont renseignés.
> - Chaque champ est accompagné de son score de confiance.
> - Si le PDF est illisible, l'OM est marqué « extraction impossible » et aucun dossier n'est créé.

Travail demandé :

1. **Rédigez 6 à 8 user stories** couvrant la fonctionnalité, chacune avec deux ou trois critères d'acceptation.
2. **Estimez-les** en planning poker (suite 1, 2, 3, 5, 8, 13).
3. **Ordonnez le backlog** : que faut-il livrer en premier, et pourquoi ?
4. **Planifiez le sprint 1** : formulez un objectif de sprint en une phrase, puis sélectionnez les stories qui le servent, dans la limite de 24 points.
5. Proposez trois lignes pour la **Definition of Done** de l'équipe.
6. Pour finir : quel rôle PRINCE2 s'intéresse à votre objectif de sprint ? Que remonte l'équipe à la cheffe de projet à la fin du sprint, et sous quelle forme ?



---

## Correction proposée


### Backlog proposé pour « Ouverture e-mail par IA – cas nominal »

| # | User story (résumé) | Points | Sprint |
|---|---|---|---|
| 1 | En tant que gestionnaire, je veux que les e-mails de la boîte « missions » et leurs pièces jointes soient relevés automatiquement, afin de ne plus surveiller la boîte | 5 | 1 |
| 2 | … que les données de l'OM soient extraites du PDF, afin de ne plus les ressaisir *(story donnée en exemple)* | 8 | 1 |
| 3 | … qu'un OM dont un champ obligatoire a un score de confiance inférieur au seuil soit placé en file de reprise, afin qu'aucun dossier douteux ne soit créé | 5 | 1 |
| 4 | … qu'un OM extrait avec confiance donne lieu à un dossier créé via l'API d'ouverture, afin que l'expert soit missionné sans attendre | 3 | 1 |
| 5 | En tant que responsable du plateau, je veux retrouver pour chaque dossier l'e-mail d'origine et les données extraites, afin de pouvoir expliquer une erreur | 3 | 1 |
| 6 | En tant que gestionnaire, je veux un écran de reprise affichant le PDF et les champs préremplis, afin de corriger et valider en moins d'une minute | 8 | 2 |
| 7 | … que les messages qui ne sont pas des OM soient écartés et laissés dans la boîte, afin qu'ils soient traités par la bonne personne | 5 | 2 |
| 8 | … qu'un OM déjà reçu (même compagnie, même numéro de sinistre) soit signalé, afin de ne pas ouvrir de doublon | 3 | 2 |
| 9 | En tant que responsable du plateau, je veux suivre chaque jour le taux d'ouverture automatique, afin de mesurer le bénéfice | 5 | 2 |
| 10 | En tant que responsable conformité, je veux que les e-mails et PDF soient purgés après 30 jours, afin de respecter le RGPD | 3 | 2 |
| | **Total** | **48** | 2 sprints |

**Objectif du sprint 1.** « Un ordre de mission PDF de la compagnie pilote, reçu par e-mail, donne un dossier créé sans intervention, ou bien est mis de côté pour reprise. »
Stories 1, 2, 3, 4 et 5 : 5 + 8 + 5 + 3 + 3 = **24 points**.

**Pourquoi cet ordre.** Le sprint 1 traverse toute la chaîne, de l'e-mail au dossier, sur un cas simple. Il répond au plus vite au risque R1 : l'IA lit-elle correctement nos documents ? L'écran de reprise (story 6) est indispensable avant la mise en production, mais pas pour apprendre.

**Exemples de critères d'acceptation (story 3).**
- Étant donné un OM dont le numéro de sinistre a un score de 62 et un seuil réglé à 80, quand l'extraction se termine, alors aucun dossier n'est créé et l'OM apparaît dans la file de reprise.
- Étant donné un OM dont tous les champs obligatoires ont un score d'au moins 80, alors il n'apparaît pas dans la file de reprise.
- Le seuil est modifiable sans nouvelle livraison.

**Definition of Done (exemple).**
- Code relu par un autre développeur et fusionné dans la branche principale.
- Tests automatisés passants dans le pipeline, critères d'acceptation vérifiés en environnement de recette.
- Aucune donnée personnelle réelle dans les jeux de tests ni dans les journaux.

### Question 6 : le lien avec PRINCE2

- L'objectif de sprint intéresse la **cheffe de projet** : la séquence S3 est découpée en lots de travaux, et les sprints en sont la réalisation. Le comité de pilotage, lui, ne suit pas les sprints : il suit la séquence.
- En fin de sprint, l'équipe fournit un **rapport de contrôle**. En pratique, la Sprint Review et le tableau de bord Azure DevOps (burndown, taux d'ouverture mesuré) en tiennent lieu : inutile de rédiger un document de plus.
- La cheffe de projet consolide ces éléments dans le **rapport de synthèse** adressé au comité de pilotage.

**Messages clés.**
- Ni les user stories, ni les story points, ni les critères d'acceptation ne figurent dans le Scrum Guide : ce sont des pratiques complémentaires. Scrum demande un Product Backlog ordonné, un objectif de sprint et une Definition of Done.
- Ce sont les développeurs qui estiment et qui choisissent ce qu'ils prennent dans le sprint ; la Product Owner ordonne et explique.
- PRINCE2 fixe le *pourquoi* et le cadre (cas d'affaire, séquences, tolérances) ; Scrum organise le *comment* à l'intérieur d'une séquence. Dans ce cas, la tolérance porte de préférence sur le périmètre : délai et coût du sprint sont fixes, c'est le contenu qui s'ajuste.
