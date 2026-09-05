# Contributing

Ce dépôt est le domicile canonique du corpus VIGILANCE. Le corpus est français et le français
fait foi ; les issues peuvent être ouvertes en français ou en anglais.

## Comment proposer

Les contributions se proposent par issue. Sont bienvenus, en particulier : les contre-exemples,
les processus réels qui mettent un mécanisme en défaut (un flux dont le « normal » ne s'écrit
pas, un taux d'exceptions qu'aucun amendement ne ramène dans une bande exploitable), les pièces
d'antériorité, les critiques, et les incohérences entre une fiche et la SPEC ; en cas de
divergence, la SPEC prévaut. Un contre-exemple nommé est un service rendu.

Les textes du corpus (SPEC, WHITEPAPER, fiches) ne se modifient que par décision de l'auteur,
tracée au CHANGELOG.

## Régimes d'écriture

Chaque document du corpus est écrit dans un **régime** déclaré. Le régime dit ce que le texte
fait et ce qu'il ne fait pas ; il n'est pas une question de style mais de rôle.

| Document | Régime | Ce qu'il fait, et ce qu'il ne fait pas |
|---|---|---|
| la [SPEC](SPEC.md) | **normatif** | Les termes, les affirmations, les règles V1.1 à V7.4, les frontières et la falsification R1 à R4. **Aucune justification, aucun exemple** : le pourquoi vit au whitepaper |
| le [WHITEPAPER](WHITEPAPER.md) | **argumentatif** | La thèse et le pourquoi de chaque famille de règles. **Il expose, il ne convainc pas** |
| les [fiches](fiches/index.md) | **pédagogique** | L'arc en six sections, voir le gabarit ci-dessous. **Elles illustrent et bornent, elles ne norment jamais** |
| le [LINEAGE](LINEAGE.md) · [research/](research/DRILL-PROTOCOLE.md) | **généalogique** | Les dettes déclarées avant l'écriture, et le protocole de banc publié avant les résultats. Le lecteur doit pouvoir prendre le corpus en défaut |
| le [README](README.fr.md) | **liminaire** | Un constat, trois ingrédients, de quoi décider d'entrer. **Il ne vend pas** |

### Le gabarit d'une fiche

Une fiche suit un arc en six sections, dans cet ordre : **Ce que c'est** · **Le geste** ·
**Un exemple** (un cas réaliste, jamais grossi ; un schéma quand il éclaire) · **Les règles qui
s'appliquent** (la fiche cite la SPEC, elle ne redéfinit pas) · **Ce que cette fiche ne promet
pas** (les bornes, dites avant qu'on les cherche) · **Rang de preuve** (jamais auto-promu ; les
rangs relèvent du protocole du laboratoire).

*Ce registre est celui de la famille ([LIVING REFERENCE](https://github.com/JP-Noto/LIVING-REFERENCE),
[WORKING REFERENCE](https://github.com/JP-Noto/WORKING-REFERENCE),
[MYSTANCE](https://github.com/JP-Noto/MYSTANCE),
[SOUNDNESS](https://github.com/JP-Noto/SOUNDNESS)) : la SPEC sèche, les fiches au registre du
professeur.*

## Statuts, crédits, licence

Le rang de l'ensemble est hypothèse, et le corpus le dit partout où il se présente : un
praticien, une mesure unique, aucun déploiement tiers ; les effets se disent au conditionnel et
la série à venir est pré-déclarée. Publié n'est pas prouvé.

Toute contribution acceptée est créditée. La licence du dépôt s'applique (LICENSE, à effet à la
publication), et le régime des contributions est déclaré d'avance, pour que personne ne le
découvre :

- une idée, un contre-exemple ou une critique proposés **par issue** sont intégrés sous la
  plume de l'auteur, et crédités ;
- un texte proposé **par pull request** emporte, s'il est accepté, l'accord de son contributeur
  pour que le titulaire du corpus l'intègre, le modifie et le licencie avec l'ensemble, y
  compris dans les accords écrits que la clause non commerciale réserve. Le contributeur reste
  crédité, et reste libre de réutiliser son propre texte ailleurs.

Une contribution qui ne souhaite pas ce régime reste une issue : elle éclaire sans entrer.

Merci de votre lecture, et de vos objections : ce corpus n'apprendra pas sans elles.
