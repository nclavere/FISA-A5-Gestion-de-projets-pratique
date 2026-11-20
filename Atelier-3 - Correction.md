# Atelier 3 – Le registre des risques (30 min dont 10 de mise en commun, en groupes)

1. Identifiez **au moins six risques** du projet. Formulez chacun en trois temps : *cause → événement → effet*.
2. Évaluez la probabilité et l'impact de chacun (de 1 à 5), puis calculez sa criticité.
3. Pour vos trois risques les plus critiques, proposez une réponse, nommez son type (éviter, réduire, transférer, partager, accepter, préparer un plan de contingence) et désignez un propriétaire.
4. Trouvez au moins une **opportunité** (un risque positif).


---

## Correction proposée

Proposition de corrigé. P = probabilité, I = impact, de 1 à 5.

| # | Cause | Événement | Effet | P | I | Criticité | Réponse (type) | Propriétaire |
|---|---|---|---|---|---|---|---|---|
| R1 | Les PDF des compagnies sont très hétérogènes | L'IA extrait mal les données | Taux de 85 % non atteint, bénéfices réduits | 4 | 5 | 20 | Tester l'IA sur 500 vrais OM dès S0, avant d'engager S3 (réduire) ; prévoir la reprise semi-automatique (plan de contingence) | Julie Perrin |
| R2 | Les règles des grands comptes ne sont documentées nulle part | Les règles sont découvertes en cours de développement | Dépassement de délai en S2 | 4 | 4 | 16 | Ateliers avec les gestionnaires experts avant S2 (réduire) | Karim Benali |
| R3 | Une compagnie fait évoluer son format de flux | Le flux n'est plus lu par le robot | Retour à la saisie manuelle, travail imprévu | 3 | 4 | 12 | Veille auprès des compagnies, budget de changement (réduire, accepter) | Inès Morel |
| R4 | Les e-mails contiennent des données personnelles envoyées à un service externe | Non-conformité RGPD constatée | Blocage de la mise en service, sanction | 2 | 5 | 10 | Clause contractuelle et hébergement en Europe (transférer, réduire) ; analyse d'impact validée avant S3 (éviter) | Marc Duval |
| R5 | Les gestionnaires craignent pour leur poste | Ils ne coopèrent pas aux ateliers et aux tests | Règles incomplètes, rejet de l'outil | 3 | 4 | 12 | Annoncer tôt le plan de redéploiement, associer le plateau aux démonstrations (réduire) | Hélène Marchand |
| R6 | L'ancien robot arrive en fin de support | Panne non réparable avant la bascule | Tout repasse en manuel | 2 | 5 | 10 | Remplacer l'ancien robot dès S1, à périmètre égal (éviter) | Thomas Leroy |
| R7 | L'équipe maintient aussi l'existant | Les développeurs sont happés par les anomalies de production | Vélocité inférieure au plan | 4 | 3 | 12 | Réserver une part de capacité à chaque sprint (accepter, réduire) | Antoine Roux |
| R8 | Le tarif du service d'IA dépend du volume | Le coût à l'usage dépasse l'hypothèse | Coût de fonctionnement supérieur à 40 k€ | 2 | 3 | 6 | Négocier un forfait (partager) | Thomas Leroy |
| O1 | Le service d'IA sait lire d'autres documents | Il peut traiter aussi factures et devis | Bénéfices supplémentaires hors projet | 3 | 3 | 9 | Concevoir l'extraction de façon réutilisable (améliorer) | Julie Perrin |

**Messages clés.**
- Exiger la formulation cause → événement → effet. « L'IA » n'est pas un risque ; « l'IA extrait mal les données » en est un.
- Distinguer le **propriétaire du risque** (il en répond) du **propriétaire des mesures** (il exécute l'action).
- Un risque est incertain ; s'il s'est déjà produit, c'est une incidence. Transition vers l'atelier 4 : R3 va se réaliser.
- R1 et R6 expliquent l'ordre des séquences : on remplace d'abord l'ancien robot, et l'on teste l'IA avant de s'engager.
