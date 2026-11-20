# Atelier 4 – Management par exception (30 min dont 10 de correction, en groupes)

Nous sommes en semaine 3 de la séquence S2. Trois événements se produisent.

- **Événement A.** Un développeur annonce que la règle « mission conjointe » de la compagnie Alpha prendra deux jours de plus que prévu.
- **Événement B.** La compagnie Bêta annonce qu'elle change le format de ses flux dans six semaines. L'ancien format ne sera plus émis. L'équipe estime l'adaptation à cinq semaines de travail pour deux développeurs : la séquence finirait avec quatre semaines de retard et coûterait 22 k€ de plus.
- **Événement C.** Karim Benali demande d'ajouter un écran permettant aux gestionnaires de corriger eux-mêmes les règles d'affectation. Estimation : 12 k€, sans effet sur la date de fin.

Pour chaque événement :

1. S'agit-il d'un risque ou d'une incidence ? De quel type ?
2. Qui décide : l'équipe, la cheffe de projet, le comité de pilotage ? Pourquoi ?
3. Quel produit de management est créé ou mis à jour ?
4. Pour l'événement B, proposez deux options à présenter au comité de pilotage.

---

## Correction proposée

| | Événement A | Événement B | Événement C |
|---|---|---|---|
| Nature | Incidence : problème ou préoccupation | Incidence, qui entraîne une requête de changement (la description du produit « flux Bêta » change) | Incidence : requête de changement |
| Qui décide | L'équipe, dans la tolérance de son lot de travaux. La cheffe de projet est informée | Le **comité de pilotage** : les prévisions dépassent les tolérances de la séquence (+ 4 semaines pour + 2 accordées ; + 22 k€ pour + 10 k€) | L'**autorité de changement**. Si le comité l'a déléguée à la cheffe de projet avec le budget de changement, c'est elle qui décide |
| Produit de management | Rapport de contrôle (de l'équipe à la cheffe de projet) ; au besoin, journal de bord | Registre des incidences, rapport d'incidence, puis **rapport d'exception** au comité ; si le comité le demande, **plan d'exception** | Registre des incidences ; budget de changement mis à jour (12 k€ sur 30 k€) ; description de produit et plan de séquence mis à jour |

**Événement B, déroulé complet.**
1. La cheffe de projet enregistre l'incidence et en évalue l'impact avec l'équipe.
2. Elle constate que la prévision sort des tolérances de la séquence : elle n'a plus autorité pour décider seule. Elle **escalade** par un rapport d'exception, sans attendre que le dépassement soit effectif.
3. Le comité de pilotage choisit une option et, le plus souvent, demande un plan d'exception qui remplacera le plan de la séquence S2.
4. Le plan d'exception est préparé dans « Gérer une limite de séquence » et approuvé dans « Diriger le projet ».

**Options à présenter au comité.**
- Reporter les règles de Delta après le projet : c'est permis par la tolérance de périmètre. S2 reste dans ses délais ; le taux visé baisse de quelques points mais reste dans la tolérance de bénéfices.
- Accepter le retard de quatre semaines sur S2 : il consomme toute la tolérance de délai du projet, il n'en reste plus pour S3, qui est la séquence la plus risquée.
- Renforcer l'équipe de deux développeurs pendant cinq semaines : coût supplémentaire, temps de montée en compétence.
- Négocier avec Bêta le maintien temporaire de l'ancien format : dépend d'un tiers.

Le budget de changement (30 k€) pourrait couvrir les 22 k€, mais il ne règle pas le dépassement de délai : l'exception demeure.

**Messages clés.**
- Trois événements, trois niveaux de décision : c'est cela, le management par exception. La direction n'est sollicitée que lorsque les tolérances sont menacées.
- On escalade sur une **prévision** de dépassement, pas sur un dépassement constaté.
- Lien avec Scrum : l'événement A se règle au Daily Scrum ; il ne remonte pas.
