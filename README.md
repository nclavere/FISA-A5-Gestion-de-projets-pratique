# FISA-A5-Gestion-de-projets-pratique

**Support pour la journée du 20/11/2026.** <br/>
*La présentation vous sera donnée au fur et à mesure, ainsi que les ateliers. <br/>
Ci-dessous, l'énoncé du projet fil rouge fictif mais tiré d'un cas réel actuel : la société, les personnes, les compagnies sont anonymisés.*<br/><br/>

--- 

# Cas fil rouge : la refonte du robot d'ouverture


## 1. Le contexte

**Eval'Expert** est un cabinet d'expertise en assurance. Quand un assuré déclare un sinistre (dégât des eaux, incendie, malfaçon…), sa compagnie d'assurance envoie au cabinet un **ordre de mission (OM)** : « allez expertiser ce sinistre ».

À la réception de chaque OM, il faut **ouvrir un dossier** dans l'application de gestion du cabinet : identifier la compagnie, l'assuré, le sinistre, le type de mission, puis affecter le dossier à la bonne agence. Tant que le dossier n'est pas ouvert, aucun expert ne peut être missionné.

### Les chiffres d'aujourd'hui

| Indicateur | Valeur |
|---|---|
| OM reçus par jour ouvré | 1 200 |
| dont par flux EDI (messages structurés) | 720 (60 %) |
| dont par e-mail (PDF en pièce jointe) | 480 (40 %) |
| OM ouverts automatiquement par le robot actuel | 540 (45 %) |
| OM ouverts à la main par les gestionnaires | 660 (55 %) |
| Temps moyen d'une ouverture manuelle | 6 minutes |
| Délai moyen d'ouverture d'un OM traité à la main | 4 heures |
| Dossiers mal qualifiés (mauvaise agence, mauvais type) | 5 % |

Le robot actuel ne sait traiter que les flux EDI au format standard. Quatre grandes compagnies (**Alpha, Bêta, Gamma et Delta**) ont des règles particulières qu'il ne gère pas : leurs 180 OM quotidiens sont saisis à la main, comme tous les e-mails.

Le robot actuel repose sur une technologie dont le support éditeur s'arrête à la fin de l'année prochaine. Sa maintenance coûte 60 k€ par an.

---

## 2. Le mandat de projet

> **De :** Hélène Marchand, directrice des opérations
> **À :** Thomas Leroy, directeur des systèmes d'information
> **Objet :** Refonte du robot d'ouverture
>
> Thomas,
>
> Comme évoqué en comité de direction, je souhaite que nous lancions la refonte de notre robot d'ouverture des dossiers.
>
> Aujourd'hui, plus d'un ordre de mission sur deux est encore saisi à la main. Nos gestionnaires y passent l'équivalent de neuf postes à temps plein, et nos clients assureurs nous reprochent des délais de prise en charge trop longs. Par ailleurs, le robot actuel ne sera bientôt plus maintenu.
>
> Mon objectif : que **85 % des ordres de mission soient ouverts automatiquement**, en moins de 15 minutes, avec moins de 2 % de dossiers mal qualifiés. Je voudrais y parvenir **en neuf mois**. Le comité de direction est prêt à engager **480 k€**.
>
> Le nouveau robot devra traiter les flux EDI, y compris les règles particulières de nos quatre grands comptes, et aussi les ordres de mission reçus par e-mail. Sur ce dernier point, regardons ce que l'intelligence artificielle permet de faire, sans perdre de vue que ces e-mails contiennent des données personnelles.
>
> Les gestionnaires libérés ne quitteront pas l'entreprise : ils seront redéployés vers le suivi des dossiers complexes. Je compte sur Karim Benali, qui dirige le plateau d'ouverture, pour porter leurs besoins.
>
> Peux-tu me revenir sous trois semaines avec une étude d'opportunité : options possibles, coûts, bénéfices, principaux risques ?
>
> Hélène

---

## 3. Les personnes

| Personne | Fonction chez Eval'Expert |
|---|---|
| Hélène Marchand | Directrice des opérations, finance le projet sur son budget |
| Thomas Leroy | Directeur des systèmes d'information (DSI) |
| Karim Benali | Responsable du plateau d'ouverture (14 gestionnaires) |
| Inès Morel | Cheffe de projet à la DSI |
| Julie Perrin | Product Owner du robot d'ouverture |
| Antoine Roux | Lead développeur de l'équipe (4 développeurs, 1 testeuse) |
| Lucas Fabre | Scrum Master de l'équipe |
| Sarah Petit | Bureau de projets (PMO) : plannings, reporting, archivage |
| Marc Duval | Responsable qualité et conformité (dont RGPD) |
| NeoDoc | Éditeur du service d'IA d'extraction de documents (fournisseur externe) |
| Compagnies Alpha, Bêta, Gamma, Delta | Clients assureurs « grands comptes » |

---

## 4. Les trois options étudiées

| | Option 0 : ne rien faire | Option 1 : refonte interne | Option 2 : solution du marché |
|---|---|---|---|
| Investissement | 0 | 480 k€ | 250 k€ (intégration) |
| Coût annuel de fonctionnement | 60 k€ (ancien robot) | 40 k€ (hébergement, IA) | 180 k€ (licences) |
| Délai de mise en service | — | 9 mois | 5 mois |
| Taux d'ouverture automatique attendu | 45 % | 85 % | 75 % (règles grands comptes mal couvertes) |
| Point d'attention | Fin de support l'an prochain | Charge de l'équipe interne | Dépendance à l'éditeur |

Hypothèses de calcul : 1 poste à temps plein = 7 heures par jour ; coût annuel d'un poste de gestionnaire = 45 k€.

---

## 5. Le plan de projet retenu (option 1)

| Séquence | Contenu | Durée | Taux d'ouverture automatique visé |
|---|---|---|---|
| S0 – Initialisation | Documentation d'initialisation du projet, architecture, backlog initial | 1 mois | 45 % (ancien robot) |
| S1 – Cas nominal | Nouvelle API d'ouverture, flux EDI standards, remplacement de l'ancien robot à périmètre égal | 2,5 mois | 45 % |
| S2 – Grands comptes | Règles particulières Alpha, Bêta, Gamma, Delta | 2 mois | 60 % |
| S3 – E-mails par IA | Lecture des OM reçus par e-mail, reprise semi-automatique | 2,5 mois | 85 % |
| S4 – Clôture | Arrêt de l'ancien robot, transfert à l'équipe produit, bilan | 1 mois | 85 % |

**Tolérances du projet** accordées par la direction :

| Aspect | Cible | Tolérance |
|---|---|---|
| Délai | 9 mois | + 4 semaines |
| Coût | 480 k€ (dont 30 k€ de budget de changement) | + 5 % |
| Périmètre | 4 grands comptes | Les règles de Delta peuvent être reportées après le projet |
| Qualité | ≤ 2 % de dossiers mal qualifiés | aucune |
| Bénéfices | 85 % d'ouverture automatique | − 5 points |

**Tolérances de la séquence S2** accordées par le comité de pilotage : 8 semaines **+ 2 semaines** ; 100 k€ **+ 10 k€**.

---