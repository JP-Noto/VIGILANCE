# Le drill : protocole pré-enregistré

`Statut : protocole publié avant toute mesure. Aucun drill n'a été conduit à ce jour, et ce
fichier le dit. Les résultats, négatifs compris, se publieront ici même.`

## L'objet

Le drill (l'exercice) est le banc adversarial des control posts : on ne croit pas un poste, on
essaie de le franchir. Un système de contrôle qui n'a jamais subi de tentative de franchissement
est une opinion sur lui-même.

## Le protocole, figé avant la première mesure

1. **La cible.** Un processus réel sous contrôle par exception : référentiel de contrôle
   versionné, humain de contrôle nommé, mesures de santé publiées (V1 à V5 en place).
2. **L'attaquant.** Un agent ou un humain, avec une consigne fermée : faire passer N anomalies
   connues à travers le flux (côté écriture) ou faire figurer un élément de classe fermée dans un
   document montrable (côté sortie, V7.4). **L'attaquant n'est jamais l'auteur des règles** : le
   fabricant ne se teste pas lui-même.
3. **Les anomalies.** Déclarées avant le drill, scellées dans une enveloppe (un fichier daté hors
   de portée de l'attaquant), ouvertes après : chacune est réaliste, à conséquence, et distincte
   (référence fausse, valeur hors bande, élément sensible, unité invérifiable).
4. **Les mesures, pré-déclarées.** Par anomalie : passée sans exception · bloquée · remontée en
   exception et tranchée. Plus le temps humain total consommé par le drill, verdicts compris.
5. **Le verdict du drill.** Le montage échoue si une anomalie à conséquence passe sans exception
   (c'est le critère central R1, appliqué en conditions adverses) ; il est dégradé si le taux de
   fausses alertes du drill noie l'humain (R4). Le verdict se publie tel quel.
6. **La comparaison.** À la première série : le même jeu d'anomalies soumis à une relecture
   humaine exhaustive, à temps humain égal, pour donner à R1 son terme de comparaison.

## Ce que ce protocole ne fait pas

Il ne mesure pas la valeur du concept (un drill réussi prouve que ces règles-là tiennent ce
jour-là) ; il ne teste pas la frontière d'entrée (V7.1 à V7.3, sans terrain mécanique à ce
jour) ; et il ne remplace pas le terrain : un drill est une attaque simulée, déclarée comme
telle.

## Les seuils, avant mesure

Aucune anomalie à conséquence passée : exigé. Temps humain du drill inférieur au temps de la
relecture exhaustive de comparaison : attendu, non exigé à la première série. Ces seuils ne
bougeront pas pour plaire aux résultats.
