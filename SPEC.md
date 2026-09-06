# SPEC VIGILANCE

`Statut : hypothèse, 0.0.1. Le normatif se dit à l'indicatif ;
le rang de l'ensemble reste hypothèse tant que la série de mesures n'existe pas.`

## Termes

- **flux** : l'ensemble des unités de travail qui passent par un processus contrôlé (les lignes
  d'un devis, les fiches d'une extraction, les livrables d'une chaîne) ; l'**unité** est la maille
  à laquelle les règles s'appliquent.
- **règle de contrôle** : un contrôle explicite du « normal » d'un flux : écrite, versionnée,
  contestable ; lisible par un humain, exécutable par le système.
- **référentiel de contrôle** : l'ensemble des règles de contrôle d'un processus. Ce qui y fait
  foi relève de LIVING REFERENCE (une référence est un élément validé) : le référentiel consomme
  les références, il ne les redéfinit pas.
- **vérification totale** : le passage de 100 % du flux par toutes les règles applicables, à
  chaque fois.
- **vigilance (du système)** : la propriété d'un processus sous vérification totale. Elle ne
  remplace pas le regard humain dû au sens de SOUNDNESS (la curation, S6 ; et, au whitepaper de
  SOUNDNESS : « la vigilance ne se délègue pas », un regard humain déclaré doit avoir eu lieu) ; elle déplace la vérification exhaustive
  vers le système pour que le regard humain restant soit réel.
- **exception** : une unité du flux qui sort d'au moins une règle. Elle remonte ; elle ne se
  corrige jamais en silence.
- **verdict** : la décision humaine sur une exception ; daté, tracé, motivé.
- **enrichissement** : la modification du référentiel de contrôle issue d'un verdict.
- **humain de contrôle** : la personne nommée qui a l'autorité de trancher les exceptions d'un
  processus (le motif du validateur nommé est hérité de SOUNDNESS).
- **ronde** : la revue asynchrone périodique du système par jugement agentique ; elle constate
  et alerte, elle ne tient jamais un contrôle en synchrone.
- **profil d'application** : le document qui porte les réglages qu'un déploiement fait des
  paramètres délégués par cette SPEC (V5.4, V6.3, V7.4) ; sans profil, les défauts de la SPEC s'appliquent.

## Les affirmations

- **A1, l'économie.** L'attention humaine est la ressource rare du processus contrôlé. Le système
  vérifie tout, l'humain ne traite que les exceptions, avec l'autorité de trancher.
- **A2, les règles lisibles.** Le « normal » se définit par des règles explicites, jamais par le
  jugement flou d'un modèle. Une règle qu'on ne peut pas lire n'est pas une règle de contrôle.
- **A3, la couverture.** La vérification est totale : chaque unité, chaque fois. L'échantillon
  n'est pas une économie, c'est un trou.
- **A4, la boucle.** Chaque verdict peut enrichir le référentiel : apprentissage organisationnel,
  pas statistique. Les exceptions d'hier deviennent les contrôles de demain.
- **A5, l'autorité.** Un contrôle constate et alerte, il n'autorise pas (hérité de MYSTANCE, M2).
  Le verdict appartient à l'humain de contrôle ; aucun réglage ne le déplace, seule l'attention se
  déplace.

## V1 — Le référentiel de contrôle

- **V1.1** Toute règle de contrôle est écrite, versionnée et datée ; elle se conteste par le même
  chemin qu'elle s'écrit.
- **V1.2** Chaque règle porte son motif et sa source : une référence validée, une obligation
  déclarée, ou le verdict qui l'a fait naître.
- **V1.3** Une règle implicite découverte en exploitation s'écrit ou se rejette, par verdict ;
  elle ne reste jamais tacite. (Occurrence fondatrice : la règle de prix « prix public × un coefficient d'usage »,
  appliquée par le métier et jamais écrite, mise au jour au premier passage sur pièce réelle.)
- **V1.4** Le jugement d'un modèle peut proposer une règle ; il n'en est jamais une. Ce que le
  système exécute au contrôle est le texte de la règle, pas une appréciation.

## V2 — La vérification totale

- **V2.1** Le système vérifie 100 % du flux contre toutes les règles applicables, à chaque
  passage. Il n'existe pas de mode « échantillon » conforme.
- **V2.2** Le système ne corrige jamais en silence : ce qui sort d'une règle remonte. (Même refus
  que SOUNDNESS S5.4 : signaler et tracer, jamais rectifier tacitement.)
- **V2.3** Une unité qui ne peut pas être vérifiée (donnée manquante, règle inapplicable) est une
  exception, pas un passage réussi.

## V3 — L'exception et le verdict

- **V3.1** Toute exception remonte à l'humain de contrôle avec la règle sortie, la valeur
  constatée et le contexte nécessaire au verdict.
- **V3.2** Le verdict prend une de ces formes, et rien d'autre : confirmer l'anomalie et la faire
  corriger ; corriger la règle (ouvrir un enrichissement, V4) ; laisser passer, motivé. Toute
  forme est datée et tracée.
- **V3.3** Un laisser-passer non motivé est la dérive nommée du système : le tampon. Il se
  compte (V5.2), il ne se néglige pas.
- **V3.4** L'humain de contrôle est nommé par processus. Une exception sans humain de contrôle
  nommé n'a pas de circuit de verdict : le processus n'est pas sous contrôle par exception.

## V4 — L'enrichissement

- **V4.1** Tout verdict qui révèle une règle manquante, fausse ou trop stricte ouvre une
  proposition d'amendement du référentiel. L'amendement est un acte tracé : décidé par un humain
  habilité (l'habilitation, SOUNDNESS S4.6), daté et consigné (au sens de la
  validation de LIVING REFERENCE, S8) ; le motif obligatoire est une exigence propre de cette
  SPEC, dans la ligne du rejet motivé de LR (S7).
- **V4.2** Le référentiel a une histoire lisible : chaque règle sait de quel verdict ou de quelle
  source elle vient (V1.2), et les amendements se relisent.
- **V4.3** Le volume seul n'amende rien : dix exceptions identiques fondent une proposition,
  jamais une décision. (Même partage que SOUNDNESS S3.2 : le système propose, il ne promeut pas.)

## V5 — Les mesures de santé

- **V5.1** Le **taux d'exceptions** se mesure et se publie au profil. Trop haut : règles trop
  strictes, ou processus malade. Zéro prolongé : règles trop lâches, ou humain décoratif. Les
  deux lectures se traitent ; aucune ne se célèbre.
- **V5.2** Le **taux de correction humaine** sur les exceptions se mesure : l'humain tranche-t-il,
  ou tamponne-t-il ? Les laisser-passer non motivés (V3.3) s'y comptent à part.
- **V5.3** L'**enrichissement dans le temps** se mesure : la part du référentiel née de verdicts,
  et la récurrence des exceptions de même cause après amendement.
  Un référentiel que plus aucun verdict n'amende est la dérive nommée de la boucle : la règle
  morte.
- **V5.4** Les seuils d'alerte de ces mesures sont délégués au profil d'application. Sans profil,
  les mesures se publient sans seuil : l'absence de profil n'est jamais un vide, c'est le défaut.

## V6 — Le control post

Le control post (en français : le poste de contrôle) est le contrôle par exception appliqué
au système lui-même : les références qui font
foi sont un flux d'écritures, et ce flux se garde.

- **V6.1** Rien n'écrit dans une référence qui fait foi hors d'un chemin d'écriture unique et
  déclaré ; le chemin s'ouvre par décision datée, puis se referme.
- **V6.2** Un garde synchrone est déterministe : un registre, une liste, une comparaison. Le
  jugement d'un modèle ne tient jamais un control post en synchrone (V1.4) ; le jugement agentique
  reste asynchrone : la ronde, jamais le control post.
- **V6.3** Un garde synchrone tient un budget de latence délégué au profil d'application
  (défaut : une seconde). Au-delà, le contrôle devient asynchrone, ou il ne se pose pas.
- **V6.4** Toute écriture bloquée au control post est une exception au sens de V3 : elle remonte avec
  la règle sortie, et le control post n'autorise rien (A5).

## V7 — La frontière avec le dehors

Le dedans étant gardé (V6), la frontière tient quatre organes : ce qui entre attend, ce qui vient
d'un tiers reste médié, ce qui est suspect s'isole, ce qui se montre se contrôle. Rang déclaré :
V7.4 a son premier terrain ; V7.1 à V7.3 sont spécifiées, non éprouvées.

- **V7.1, le sas (airlock).** Rien n'entre directement dans le périmètre de ce qui fait foi :
  tout contenu entrant attend dans un lieu de dépôt distinct, hors du périmètre, jusqu'à
  qualification par acte. Jamais les deux portes ouvertes : le geste qui dépose n'est jamais le
  geste qui promeut.
- **V7.2, le parloir (parlor).** Un contenu tiers n'écrit jamais dans ce qui fait foi par
  lui-même : il passe par une médiation qui le lit comme matière, jamais comme instruction.
- **V7.3, la quarantaine (quarantine).** Un élément suspect ne se détruit ni ne s'admet : il
  s'isole avec sa trace, en état déclaré, en attente de verdict (V3). Une quarantaine n'est
  jamais un oubli : elle se compte à la ronde.
- **V7.4, le poste de sortie (exit post).** Ce qui se montre se contrôle comme ce qui s'écrit :
  tout document destiné à l'exposition porte une classe de diffusion déclarée, et un control post
  de sortie vérifie qu'aucun élément d'une classe plus fermée n'y figure. Les classes et leurs
  noms sont délégués au profil d'application ; le verdict d'exception reste humain (V3, A5).

## Frontières

- **Ce que VIGILANCE ne régit pas.** L'admission au canon (LIVING REFERENCE) est un acte
  d'attention pleine sur chaque élément candidat : elle n'est pas un flux à mettre sous contrôle
  par exception, et cette SPEC ne s'y applique pas.
- **Ce que VIGILANCE ne promet pas.** Cette SPEC norme une économie de l'attention face à
  la dérive ordinaire (l'erreur, l'oubli, le glissement), pas un dispositif de sécurité :
  la sécurité suppose un adversaire actif, qui lit les règles pour les contourner, et rien
  ici ne prétend lui résister. V6 et V7 empruntent des organes à la sûreté des systèmes ;
  l'emprunt est déclaré (WHITEPAPER, travaux voisins ; LINEAGE), il ne transfère pas la
  garantie.
- **La frontière travail/personnes.** La vigilance porte sur les productions et les
  processus, jamais sur les personnes : le contrôle qualité des livrables n’est pas la
  surveillance de ceux qui les font, qui relève d’un autre régime (droit du travail,
  protection des données) et que cette SPEC n’outille ni n’autorise.
- **La frontière avec MYSTANCE.** Quand l'humain tamponne, le versant relation relève de
  MYSTANCE (la souveraineté, M2 ; l'angle mort du coupable commode de son whitepaper) ;
  VIGILANCE dit comment le flux le rend visible (un taux, V5.2). Deux faces du même phénomène, deux corpus, aucun ne redéfinit l'autre. Le mot « médiation » s'emploie dans cette SPEC comme nom
  commun (V7.2) ; il ne désigne jamais MÉDIATION, le premier niveau d'assistance de MYSTANCE.
- **La frontière avec WORKING REFERENCE.** L'humain à la gate, jamais à l'appel : la
  formule condense ce que WR décide en C2 (rien n'entre dans la constante
  que par une gate datée) et I2 (aucun jugement d'auteur requis à l'appel). VIGILANCE y lit une
  économie de l'attention, la nomme en principe général et apporte la mesure ; WR reste le
  mécanisme de preuve côté référence.
- **La frontière avec SOUNDNESS.** La curation du savoir extrait reste normée par SOUNDNESS
  (S6 : le tamis dit ce qui est dû, et seulement lui) ; VIGILANCE nomme le principe général et
  fournit la mesure, il ne s'empile pas sur ce flux. La qualification de ce qui entre (déclaration, canal, statut)
  reste normée par SOUNDNESS de même ; V7 tient la frontière elle-même : l'attente, la médiation,
  l'isolement, l'exposition. Aucun des deux ne redéfinit l'autre.
- **L'antériorité du concept.** Le contrôle par exception descend du *management by exception* ;
  l'apport revendiqué est l'assemblage (règles lisibles + vérification totale exécutable par
  l'IA + boucle de verdicts, mesuré), pas l'idée. Le détail vit au WHITEPAPER (travaux voisins)
  et au LINEAGE.

## Falsification

- **R1** (le critère central, publié avant toute série) :
  si, sur un processus réel instrumenté, le contrôle par exception laisse passer davantage
  d'anomalies à conséquence que la relecture humaine exhaustive qu'il remplace, à temps humain
  égal ou supérieur, le concept tombe.
- **R2** : si un processus réel exige durablement, pour distinguer son « normal », un jugement
  qui ne s'exprime pas en règle lisible (V1), A2 est réfuté sur ce domaine, et le domaine se
  déclare.
- **R3** : si l'enrichissement (V4) ne réduit pas la récurrence des exceptions de même cause sur
  la durée du profil, A4 est réfuté.
- **R4** : si le taux d'exceptions ne peut être tenu dans une bande exploitable (ni noyade, ni
  zéro prolongé) malgré l'amendement des règles, l'économie revendiquée par A1 n'existe pas sur
  ce processus.
