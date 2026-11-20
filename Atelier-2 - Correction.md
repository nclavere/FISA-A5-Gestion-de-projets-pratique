# Atelier 2 – Le cas d'affaire (30 min dont 10 de correction, en groupes)

À partir des sections 1 et 4 :

1. Calculez, pour les options 1 et 2, le nombre de postes libérés et le gain annuel net.
2. Calculez le délai de retour sur investissement de chaque option.
3. Citez un **livrable**, un **résultat**, un **bénéfice** et un **contre-bénéfice** du projet.
4. Quelle option recommandez-vous ? Quel argument pourrait faire pencher pour l'autre ?
5. Qui vérifiera que les bénéfices sont atteints, et quand ?


---

## Correction proposée

**Situation actuelle.** 660 ouvertures manuelles × 6 min = 3 960 min = 66 h par jour, soit 66 / 7 = **9,4 postes**.

| | Option 1 : refonte interne | Option 2 : solution du marché |
|---|---|---|
| Ouvertures manuelles restantes | 15 % × 1 200 = 180 par jour | 25 % × 1 200 = 300 par jour |
| Charge restante | 180 × 6 min = 18 h, soit 2,6 postes | 300 × 6 min = 30 h, soit 4,3 postes |
| Postes libérés | 9,4 − 2,6 = **6,8** | 9,4 − 4,3 = **5,1** |
| Gain de main-d'œuvre | 6,8 × 45 k€ = 306 k€ | 5,1 × 45 k€ = 230 k€ |
| Ancien robot supprimé | + 60 k€ | + 60 k€ |
| Nouveau coût de fonctionnement | − 40 k€ | − 180 k€ |
| **Gain annuel net** | **326 k€** | **110 k€** |
| Investissement | 480 k€ | 250 k€ |
| **Retour sur investissement** | 480 / 326 = **1,5 an** | 250 / 110 = **2,3 ans** |
| Bilan à 3 ans | 3 × 326 − 480 = **+ 498 k€** | 3 × 110 − 250 = **+ 80 k€** |

**Question 3.**
- Livrable : le nouveau robot d'ouverture (API, règles, lecture des e-mails).
- Résultat : 85 % des OM ouverts sans intervention, en moins de 15 minutes.
- Bénéfice : 326 k€ nets par an ; prise en charge plus rapide pour les assureurs.
- Contre-bénéfice : inquiétude et réorganisation du plateau (14 gestionnaires à redéployer et former) ; dépendance à un service d'IA externe.

**Question 4.** Option 1. L'argument pour l'option 2 : elle est en service quatre mois plus tôt et fait porter le risque de réalisation à l'éditeur. Si la fin de support de l'ancien robot était dans six mois, elle deviendrait sérieuse. L'option 0 n'est pas tenable, mais elle doit toujours figurer : c'est la référence de comparaison.

**Question 5.** Les bénéfices arrivent **après** la clôture du projet. L'approche de gestion des bénéfices dit qui les mesure et quand : ici Karim Benali, qui suit le taux d'ouverture automatique et le nombre de postes redéployés, par exemple 3, 6 et 12 mois après la mise en service. L'exécutif en reste responsable.

**Messages clés.**
- Le cas d'affaire n'est pas écrit une fois pour toutes : il est revu à chaque fin de séquence (principe de justification continue).
- Le poste « gain de main-d'œuvre » n'existe que si les gestionnaires sont réellement redéployés. C'est un bon point de débat sur la sincérité des cas d'affaire.
