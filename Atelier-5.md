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
