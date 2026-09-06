# VIGILANCE

**Pour que l'humain se concentre là où il a de la valeur.**

> Maxime fondatrice : « L'humain concentré là où il a de la valeur, le système vigilant partout. »

`Statut : Public Draft · Corpus : 0.1.2 · Rang : banc d'essai · Licence : CC BY-NC-SA 4.0`

> **Étage de ce travail : banc d'essai** (gate 2 franchie le 2026-09-06, décision signée ; l'hypothèse reste la forme, et le drill reste à conduire). Un praticien, un processus instrumenté, une mesure (un devis,
> contrôle inclus, passe de 65-90 minutes à 25). Rien de répliqué, rien de démontré. « Prouvé »
> exigerait une série ; la série n'existe pas encore. Les résultats négatifs se publieront comme
> les autres.

Le français fait foi. English readers: see [README.md](README.md).

## Le constat

Deux façons de contrôler le travail, et les deux échouent quand le volume monte. La relecture
humaine exhaustive ne passe pas à l'échelle : elle fabrique le tampon-buvard, l'humain qui signe
sans voir. Le contrôle par échantillon passe à l'échelle : il laisse passer l'aiguille.

## Le principe : le contrôle par exception

Le système vérifie 100 % du flux contre des règles explicites ; l'humain ne traite que ce qui en
sort, avec l'autorité de trancher. Trois ingrédients, tous nécessaires :

1. **Des règles explicites du « normal »** : écrites, versionnées, contestables. Pas un jugement
   flou du modèle : des contrôles qu'on peut lire.
2. **La vérification totale par le système** : chaque ligne, chaque fois. L'IA rend la vigilance
   exhaustive abordable.
3. **L'humain sur les seules exceptions** : et chaque exception jugée enrichit les règles.
   Apprentissage organisationnel, pas statistique.

La couverture est totale et l'attention humaine est réelle : la combinaison que ni la relecture
exhaustive ni l'échantillon n'offrent.

## Une surveillance permanente ? Non : deux régimes

La question vient tôt, et elle est légitime : si le système vérifie tout, est-ce une
surveillance permanente ? Non. Le contrôle a deux régimes, chacun sur son objet, et rien ne
tourne entre les deux.

**Le flux, d'abord** : tout ce que le système produit ou laisse entrer, unité par unité.
Un devis fournisseur qui arrive et se contrôle ligne à ligne, une écriture dans le
référentiel des prix, une fiche mise à jour, un document qui part vers un tiers : chaque
unité de ce flux est un « passage ».

- **Au passage** : à chaque unité produite. Cent pour cent du flux, à chaque passage (V2),
  sur un chemin d'écriture unique où des gardes déterministes tranchent dans un budget de
  latence (V6). Déclenché par l'acte, jamais entre deux actes : tant que rien ne se
  produit, rien ne tourne.
- **À la ronde** : périodiquement, sur l'état global. La revue asynchrone par jugement
  agentique constate ce qu'aucun passage ne peut voir : le lien qui pourrit, le fichier
  modifié hors du chemin, l'invariant global qui s'est défait.

Un contrôle permanent n'ajouterait aucune garantie : entre deux actes, rien ne change par
le chemin ; ce qui change hors du chemin est précisément une anomalie que la ronde
constate. Il ajouterait du coût et du bruit, ce que l'économie de l'attention refuse. La
limite se déclare : entre deux rondes, une modification hors chemin reste invisible ;
c'est pourquoi le chemin unique est une règle (V6.1), être hors du chemin est une anomalie
en soi.
## Ce que le corpus mesure

- **Le taux d'exceptions.** Trop haut : règles trop strictes, ou processus malade. Zéro : règles
  trop lâches, ou humain décoratif.
- **Le taux de correction humaine sur les exceptions** : l'humain tranche-t-il, ou tamponne-t-il ?
- **L'enrichissement des règles dans le temps** : les exceptions d'hier deviennent les contrôles
  de demain.

## Ce qui invaliderait le concept

Sur un processus réel instrumenté : si le contrôle par exception laisse passer davantage
d'anomalies à conséquence que la relecture humaine exhaustive qu'il remplace, à temps humain égal
ou supérieur, le concept tombe. Le critère est publié avant les séries de mesure, et il ne
bougera pas pour leur plaire.

**Ce que le corpus ne promet pas.** VIGILANCE économise l'attention face à la dérive
ordinaire : l'erreur, l'oubli, le glissement. Ce n'est pas un dispositif de sécurité. La
sécurité suppose un adversaire actif, qui lit les règles pour les contourner ; ce corpus ne
promet rien contre lui, et les champs qui traitent l'adversaire sont nommés au
[WHITEPAPER](WHITEPAPER.md) (travaux voisins) et au [LINEAGE](LINEAGE.md). Et une seconde
frontière, sœur de la première : **la vigilance porte sur les productions et les processus,
jamais sur les personnes**. Le contrôle qualité des livrables n’est pas la surveillance de
ceux qui les font : cet usage relève d’un autre régime, et ce corpus ne l’outille pas. Les mesures de santé
du corpus lisent des règles et des processus, jamais des personnes
([Mesures de santé](fiches/MESURES-DE-SANTE.md)).

## D'où il vient

Né sur un terrain réel le 2026-08-06 : une seconde paire d'yeux humaine remplacée par cinq
contrôles mécaniques sur des devis fournisseurs. Premier passage sur pièce le lendemain : neuf
exceptions remontées, dont deux invisibles au prix (qui auraient livré le
produit A à la place du produit B), et une règle implicite du métier mise au jour,
jamais écrite. Première mesure le 2026-09-04 : un devis, contrôle inclus, de 65-90 minutes à 25.
Le détail daté vit dans [LINEAGE](LINEAGE.md).

## La famille

Ce corpus est le cinquième d'une famille, et chaque couche a son rôle :

| Couche | Gouverne |
|---|---|
| Un OS d'IA (tiers) | le système : lois, fichiers, boucles, frontières |
| [LIVING REFERENCE](https://github.com/JP-Noto/LIVING-REFERENCE) | le statut du savoir : ce qui est validé, ce qui fait canon |
| [WORKING REFERENCE](https://github.com/JP-Noto/WORKING-REFERENCE) | le service de la référence : ce qui monte à l'appel, servi et scellé |
| [MYSTANCE](https://github.com/JP-Noto/MYSTANCE) | la place de l'humain : la relation paramétrée, la montée en compétence, la souveraineté |
| [SOUNDNESS](https://github.com/JP-Noto/SOUNDNESS) | la naissance du savoir extrait de documents : la fiche fondée sur la pièce |
| **VIGILANCE** | l'économie de l'attention humaine : le contrôle par exception, l'humain sur les seules exceptions |

VIGILANCE porte le chaînon entre les couches : il consomme les références des aînés, il ne les
redéfinit pas. La doctrine est indépendante de tout OS hôte et de tout modèle, présents ou
futurs ; une indépendance par construction, les corpus étant du texte ; l'épreuve opérationnelle est
au banc. La
famille est opérée par le laboratoire ONDE AI R&D — son portail : <https://github.com/JP-Noto/ONDE>.

## Les documents

| Document | Rôle |
|---|---|
| [SPEC](SPEC.md) | le normatif : termes, cinq affirmations, familles V1-V7, frontières, falsification R1-R4 ; il prime |
| [WHITEPAPER](WHITEPAPER.md) | le pourquoi de chaque ingrédient, le cas fondateur avec ses rangs de preuve, les travaux voisins |
| [LINEAGE](LINEAGE.md) | les dettes déclarées avant l'écriture, et la généalogie interne datée |
| [fiches/](fiches/index.md) | neuf fiches de praticien : la revendication, le geste, l'exemple, ce que la fiche ne promet pas |
| [research/](research/DRILL-PROTOCOLE.md) | le drill : protocole de banc adversarial, pré-enregistré avant toute mesure |
| [profiles/](profiles/DEVIS.md) | un profil d'application déclaré par terrain (le contrôle de devis, dé-marqué) |
| [README.md](README.md) | le miroir anglais ; le français fait foi |
| [CHANGELOG](CHANGELOG.md) · [CITATION.cff](CITATION.cff) · [LICENSE](LICENSE.md) · [CONTRIBUTING](CONTRIBUTING.md) | versions, citation, licence, état des contributions |
