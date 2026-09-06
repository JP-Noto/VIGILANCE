# Profil d'application : le contrôle de devis

`Statut : profil déclaré, premier terrain du corpus (N=1, chez le praticien). Un profil porte les
réglages que la SPEC délègue ; sans profil, les défauts de la SPEC s'appliquent.`

## Le processus

Le contrôle de devis fournisseurs avant engagement. L'unité : la ligne de devis. Le flux :
chaque ligne de chaque devis, à chaque réception.

## Le référentiel de contrôle (V1)

Cinq familles de règles, versionnées avec le profil :

| Règle | Ce qu'elle vérifie |
|---|---|
| référence | la référence existe au catalogue du fournisseur, et correspond à la désignation |
| désignation | la désignation ne contredit pas la référence (le produit A n'est pas le produit B) |
| tarif | le prix unitaire est celui du tarif en vigueur |
| prix public | le prix public de référence est celui du catalogue daté |
| coefficient | le prix de vente vaut le prix public × le coefficient d'usage déclaré, dans sa bande |

## Les réglages délégués

| Paramètre | Délégation | Valeur du profil |
|---|---|---|
| seuils d'alerte des mesures (V5.4) | profil | taux d'exceptions attendu : quelques lignes par devis ; zéro prolongé sur dix devis : alerte |
| budget de latence des gardes (V6.3) | profil | défaut de la SPEC : une seconde |
| classes de diffusion (V7.4) | profil | PRIVÉ (ne quitte jamais le poste de travail) · INTERNE (jamais affiché à un tiers) · MONTRABLE (zéro élément sensible) |

## L'humain de contrôle (V3.4)

La personne qui engage le devis. Le verdict est le sien ; le contrôle constate et alerte, il
n'autorise pas.

## La mesure fondatrice, déclarée

Un devis, contrôle inclus : de 65-90 minutes à 25 (un point de donnée, chez le praticien, le
2026-09-04). Premier passage sur pièce réelle : quinze lignes, sept fournisseurs, neuf exceptions
remontées, dont deux références fausses invisibles au prix. Un second point de donnée, de fond, consigné le 2026-09-06 : sur un dossier à cinq
chiffres, le bon de commande client portait une dimension conforme à la liste de prix qui
fait foi ; le devis fournisseur s’était autorisé à changer la dimension minimale. L’écart,
remonté en exception avant engagement, a fait exiger une pièce conforme à la liste de prix
et a évité un litige client sur une seule référence.

Rien de répliqué ; la série à venir
est pré-déclarée au WHITEPAPER.

## Le modèle de menace du profil

Trois champs, déclarés pour que la limite de sécurité se lise au point d’usage.

**Adversaire supposé** : le document de tiers lui-même (un devis reçu peut porter des
instructions ou des données forgées que l’agent lit : injection indirecte) ; et l’erreur non
malveillante du fournisseur, qui reste le cas dominant.

**Parades effectives** : le référentiel V1 versionné avec le profil ; le verdict humain V3.4
(le contrôle constate et alerte, il n’autorise jamais) ; les classes de diffusion V7.4 ; la
lecture seule du flux de contrôle.

**Hors périmètre** : l’adversaire actif persistant ; la collusion de l’humain de contrôle ;
l’authentification de la pièce source (la provenance est tracée, la pièce n’est pas
authentifiée) ; le déni de service. Les deux phrases de périmètre du corpus s’appliquent.

## Ce que ce profil ne dit pas

Les valeurs du coefficient et des bandes appartiennent au déploiement, pas au corpus. Ce profil
est un exemple déclaré, pas un modèle : un autre processus élira d'autres règles, d'autres
seuils, d'autres classes, par le même chemin.
