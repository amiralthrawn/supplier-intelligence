# supplier-intelligence
Supplier and procurement intelligence system for wholesale businesses

Le problème est maintenant beaucoup plus clairement défini

Je le formaliserais ainsi :

Un grossiste qui dépend de fournisseurs historiques (fixe) dispose d'une excellente connaissance de ses propres fournisseurs, mais d'une visibilité insuffisante sur la compétitivité réelle du marché.

Cela crée plusieurs risques :

risque prix : son fournisseur augmente ses tarifs alors que le marché baisse ;
risque de dépendance : il n'a pas d'alternative immédiatement identifiée ;
risque logistique : un fournisseur devient moins performant sur les délais ou les coûts de transport ;
risque qualité : qualité variable du produit en fonction des périodes selon sa provenance ;
risque commercial : conditions de paiement, MOQ, volumes disponibles, etc. ;
risque d'opportunité : un concurrent devient beaucoup plus intéressant et le grossiste ne le sait pas.

Mon produit ne dit pas :

« Changez de fournisseur. »

Il dit :

« Voici objectivement où se situe votre fournisseur par rapport aux alternatives disponibles sur le marché. »

C'est une distinction fondamentale.


Collaboration indispensable avec les spécialistes du marché

Je ne peux pas devenir expert simultanément en :

pétrole ;
cacao ;
kaolin ;
huiles végétales ;
farine ;
actifs cosmétiques ;
etc.

Mon role est seulement :

Data / Intelligence

Je construis :

pipeline de données ;
nettoyage ;
normalisation ;
comparaison ;
statistiques ;
modèles ;
scoring ;
détection d'anomalies ;
simulation ;
dashboard / reporting.


L'expert du grossiste : Procurement / Commodity

Il m'apporte :

connaissance des fournisseurs ;
qualité acceptable ;
contraintes réglementaires ;
spécifications techniques ;
saisonnalité ;
réalité du marché ;
fournisseurs réellement crédibles ;
informations difficiles à obtenir automatiquement.


Le système combine les deux.

C'est beaucoup plus crédible qu'un système prétendant tout savoir et tout regler automatiquement.




                                 ┌──────────────────────┐
                                 │       GROSSISTE      │
                                 │        CLIENT        │
                                 └──────────┬───────────┘
                                            │
                                            ▼
                              ┌───────────────────────────┐
                              │ 1. BESOIN / PROBLÈME      │
                              │                           │
                              │ Manque de visibilité sur  │
                              │ la compétitivité de ses   │
                              │ fournisseurs              │
                              └─────────────┬─────────────┘
                                            │
                                            ▼
                     ┌──────────────────────────────────────────┐
                     │       2. ACQUISITION DES DONNÉES         │
                     └─────────────────────┬────────────────────┘
                                           │
             ┌─────────────────────────────┼─────────────────────────────┐
             │                             │                             │
             ▼                             ▼                             ▼

   DONNÉES DÉJÀ DISPONIBLES       DONNÉES À OBTENIR              DONNÉES À ACQUÉRIR
          CHEZ LE CLIENT            PAR LE CLIENT                  PAR NOUS
             │                             │                             │
             │                             │                             │
     ┌───────┴────────┐            ┌───────┴────────┐          ┌─────────┴─────────┐
     │                │            │                │          │                   │
     ▼                ▼            ▼                ▼          ▼                   ▼
Données sur       Données de    Informations    Données     Données marché    Données marché
ses propres       marché déjà   que le client   obtenues   publiques          spécialisées    ------->  
fournisseurs      connues       va rechercher   auprès de   accessibles        payantes
                                  lui-même      sources
     │                │            │                │          │                   │
     │                │            │                │          │                   │
     │                │            │                │          │                   │
     │                │            │                │          │                   │
     │                │            │                │          │                   │
     └────────────────┴────────────┴────────────────┴──────────┴───────────────────┘
                                           │
                                           ▼
                              ┌───────────────────────────┐
                              │ 3. TRI / SÉLECTION DATA   │
                              │                           │
                              │ Quelles données sont      │
                              │ pertinentes pour l'offre │
                              │ du client ?               │
                              └─────────────┬─────────────┘
                                            │
                                            ▼
                              ┌───────────────────────────┐
                              │ 4. QUALIFICATION DES      │
                              │         DONNÉES           │
                              │                           │
                              │ Qualité                   │
                              │ Fraîcheur                 │
                              │ Provenance                │
                              │ Couverture                │
                              └─────────────┬─────────────┘
                                            │
                                            ▼
                              ┌───────────────────────────┐
                              │ 5. DATA RELIABILITY       │
                              │         SCORE             │
                              │          /100             │
                              └─────────────┬─────────────┘
                                            │
                                            ▼
                              ┌───────────────────────────┐
                              │ 6. NORMALISATION DATA     │
                              └─────────────┬─────────────┘
                                            │
                                            ▼
                              ┌───────────────────────────┐
                              │ 7. MARKET BENCHMARK       │
                              └─────────────┬─────────────┘
                                            │
                                            ▼
                              ┌───────────────────────────┐
                              │ 8. SUPPLIER ANALYSIS      │
                              │                           │
                              │ Prix                      │
                              │ Qualité                   │
                              │ Délais                    │
                              │ Logistique                │
                              │ Conditions commerciales   │
                              │ etc.                      │
                              └─────────────┬─────────────┘
                                            │
                              ┌─────────────┴─────────────┐
                              ▼                           ▼
                     SUPPLIER PERFORMANCE        RISK / EXPOSURE
                          SCORE                   DEPENDANCE
                              │                           │
                              └─────────────┬─────────────┘
                                            ▼
                              ┌───────────────────────────┐
                              │ 9. OPPORTUNITY ENGINE     │
                              └─────────────┬─────────────┘
                                            │
                                            ▼
                              ┌───────────────────────────┐
                              │ 10. RECOMMANDATION ACHATS │
                              └─────────────┬─────────────┘
                                            │
                              ┌─────────────┼─────────────┐
                              ▼             ▼             ▼
                         RENÉGOCIATION  ALTERNATIVE   MAINTIEN


2. Acquisition des données

A — Données déjà disponibles chez le client

Ce que le grossiste possède déjà dans ses systèmes/documents :

fournisseurs actuels ;
prix d'achat ;
volumes ;
historique ;
délais ;
qualité ;
transport ;
conditions de paiement ;
contrats ;
etc.

B — Informations de marché déjà connues par le client

Et ça, c'est différent.

Le client peut déjà savoir :

que son fournisseur vend également à d'autres entreprises ;
que certains clients paient moins/plus cher ;
qu'il existe d'autres fournisseurs ;
qu'un fournisseur concurrent est réputé intéressant ;
qu'une certaine origine est meilleure ;
etc.

Ce sont des informations de marché détenues par le client, même si elles ne sont pas dans son ERP.

C — Données que le client va chercher lui-même

Le client peut dire :

« Je connais trois fournisseurs supplémentaires, je vais les contacter et leur demander un devis. »

Je récupères ensuite ces informations et je les intègres au système.

C'est important parce que je ne paie pas l'acquisition, mais la donnée peut être extrêmement intéressante.

D — Données publiques que Je recherches

C'est la première partie d'offre :

Données client
+
Données marché déjà connues
+
Données obtenues par le client
+
Données publiques recherchées par moi
        ↓
PREMIÈRE ANALYSE

Je peux aller chercher des informations supplémentaires pour couvrir la fiabilité des donnée transmise par le fournisseur initial et aussi pour intégrer de nouveau fournisseur à l'analyse. 

fournisseurs ;
catalogues ;
prix publiés ;
informations commerciales ;
certifications ;
pays d'origine ;
capacités apparentes ;
données douanières ;
indices ;
etc.

E — Données supplémentaires nécessitant une acquisition

Et là, on arrive aux offres supérieures.

Certaines données :

ne sont pas publiques ;
sont payantes ;
nécessitent une base spécialisée ;
nécessitent un accès professionnel ;
nécessitent une collecte humaine.

Je peux donc les acheter directement.

Et enfin :

F — Données nécessitant une collecte sous-traitée

Lorsque la collecte nécessite :

sourcing spécialisé ;
appels ;
demandes de devis ;
vérifications ;
expertise sectorielle ;
enquête de marché ;

Je fais intervenir une agence, un expert ou un prestataire spécialisé.


Si on observe que Concurrent X → fournisseur Y

on ne peut pas conclure :

« Fournisseur Y peut proposer au client 7,20 €/kg. »

On peut seulement conclure :

« Fournisseur Y constitue une source potentielle à investiguer. »  

Et ça change la façon dont je construirais le produit


                   Grossiste
                       │
                       ↓
                DONNÉES INTERNES
                       │
                       ↓
              ┌─────────────────┐
              │ DATA ENGINE     │
              │                 │
              │ Normalisation   │
              │ Benchmark       │                    Partie 1 de l'offre (traitement de donnée interne + source de marché accessible) 
              │ Scoring         │
              │ Statistics      │
              │ Simulation      │
              └────────┬────────┘
                       ↑
                       │
          DONNÉES DE MARCHÉ (sous traité)
                       ↑
                       │
          ┌────────────┼────────────┐                Partie 2 de l'offre (ajout de traitement de données de marché) le client paie pour : 
          │            │            │                . recherches de fournisseurs supplémentaires 
       Agence       Expert       Database            . données de marché spécialisées 
       sourcing     marché       spécialisée         . collecte de devis 
                                                     . vérifications de certaines informations 
                                                     . données commerciales professionnelles.


Partie 3 — Continuous Intelligence

Le client veut que le système soit surveillé régulièrement.

Par exemple :

Analyse mensuelle / trimestrielle.

Le prestataire ou les sources externes alimentent la base.

Le système recalcule :

benchmark ;
Supplier Performance Index ;
évolution des prix ;
évolution de la compétitivité ;
opportunités de négociation ;
alternatives.

                    
                        GROSSISTE
                            │
                            ▼
              ┌──────────────────────────┐
              │  DONNÉES INITIALEMENT    │
              │       DISPONIBLES        │
              └────────────┬─────────────┘
                           │
             ┌─────────────┴─────────────┐
             │                           │
             ▼                           ▼
      Données fournies             Données recherchées
        par le client                 par nous
             │                           │
             └─────────────┬─────────────┘
                           ▼
                  PREMIÈRE ANALYSE
                           │
                           ▼
                  ┌────────────────┐
                  │   PRÉSENTATION │
                  │   AU CLIENT    │
                  └───────┬────────┘
                          │
                    SI LE CLIENT
                      ACCEPTE
                          │
                          ▼
════════════════════════════════════════════════════════════
                    PARTIE 1 — ANALYSE
════════════════════════════════════════════════════════════

        Données supplémentaires obtenues
        directement avec le client
                 │
                 │
          ┌──────┴──────┐
          ▼             ▼
      Pôle Data     Informations
       du client    supplémentaires
                    sur fournisseurs
                    / marché
          │             │
          └──────┬──────┘
                 ▼
          DONNÉES ENRICHIES
                 │
                 ▼
       QUALIFICATION / FIABILITÉ
                 │
                 ▼
              ANALYSE
                 │
                 ▼
            SCORE /100


════════════════════════════════════════════════════════════
                    PARTIE 2 — UPSELL
════════════════════════════════════════════════════════════

              BESOIN SPÉCIFIQUE DU CLIENT
                         │
                         ▼
             DONNÉES PRIVÉES / PAYANTES
                         │
                         ▼
                    ACQUISITION
                         │
                         ▼
                  DONNÉES ENRICHIES
                         │
                         ▼
                  ANALYSE ACTUALISÉE
                         │
                         ▼
                       SCORE


════════════════════════════════════════════════════════════
                    PARTIE 3 — UPSELL
════════════════════════════════════════════════════════════

              BESOIN SPÉCIFIQUE DU CLIENT
                         │
                         ▼
             DONNÉES DIFFICILES D'ACCÈS
                         │
                         ▼
              SOUS-TRAITANCE EXTERNE
                         │
                 ┌───────┼───────┐
                 ▼       ▼       ▼
              Agence   Expert   Sourcing
                         │
                         ▼
                  DONNÉES ENRICHIES
                         │
                         ▼
                  ANALYSE ACTUALISÉE
                         │
                         ▼
                       SCORE


════════════════════════════════════════════════════════════
                 PARTIE 4 — CONTINUOUS INTELLIGENCE
════════════════════════════════════════════════════════════

                    DONNÉES MISES À JOUR
                            │
                            ▼
                     ANALYSE CONTINUE
                            │
             ┌──────────────┼──────────────┐
             ▼              ▼              ▼
        Évolution       Évolution      Nouvelles
          prix        fournisseurs    opportunités
             │              │              │
             └──────────────┼──────────────┘
                            ▼
                     SCORE ACTUALISÉ
                            │
                            ▼
                    ALERTES / RAPPORTS



                                    ┌──────────────────────────────┐
                                    │           GROSSISTE          │
                                    └──────────────┬───────────────┘
                                                   │
                                                   ▼
                               ┌──────────────────────────────────────┐
                               │   DONNÉES INITIALEMENT DISPONIBLES   │
                               └────────────────────┬─────────────────┘
                                                    │
                          ┌─────────────────────────┴─────────────────────────┐
                          │                                                   │
                          ▼                                                   ▼
              ┌──────────────────────┐                            ┌──────────────────────┐
              │ DONNÉES FOURNIES     │                            │ DONNÉES RECHERCHÉES  │
              │ PAR LE CLIENT        │                            │ PAR NOUS             │
              └──────────┬───────────┘                            └──────────┬───────────┘
                         │                                                   │
                         └──────────────────────┬────────────────────────────┘
                                                ▼
                                   ┌─────────────────────────┐
                                   │    PREMIÈRE ANALYSE     │
                                   └────────────┬────────────┘
                                                │
                                                ▼
                                   ┌─────────────────────────┐
                                   │   PRÉSENTATION CLIENT   │
                                   └────────────┬────────────┘
                                                │
                               ┌────────────────┴────────────────┐
                               │                                 │
                               ▼                                 ▼
                   ┌──────────────────────┐          ┌──────────────────────┐
                   │ CLIENT N'ACCEPTE PAS │          │   CLIENT ACCEPTE     │
                   └──────────┬───────────┘          └──────────┬───────────┘
                              │                                 │
                              ▼                                 ▼
                     ┌────────────────┐              ╔══════════════════════╗
                     │ FIN DE MISSION │              ║      PARTIE 1        ║
                     └────────────────┘              ║  ENRICHISSEMENT AVEC ║
                                                     ║      LE CLIENT       ║
                                                     ╚══════════╤═══════════╝
                                                                │
                                       ┌────────────────────────┴────────────────────────┐
                                      │                                                 │
                                      ▼                                                 ▼
                           ┌────────────────────┐                          ┌────────────────────────┐
                           │     PÔLE DATA      │                          │ INFORMATIONS           │
                           │     DU CLIENT      │                          │ SUPPLÉMENTAIRES        │
                           └─────────┬──────────┘                          │ FOURNISSEURS / MARCHÉ  │
                                     │                                     └───────────┬────────────┘
                                     └──────────────────────┬──────────────────────────┘
                                                            ▼
                                                ┌──────────────────────┐
                                                │  DONNÉES ENRICHIES   │
                                                └──────────┬───────────┘
                                                           ▼
                                                ┌──────────────────────┐
                                                │ QUALIFICATION /      │
                                                │     FIABILITÉ        │
                                                └──────────┬───────────┘
                                                           ▼
                                                ┌──────────────────────┐
                                                │       ANALYSE         │
                                                └──────────┬───────────┘
                                                           ▼
                                                ┌──────────────────────┐
                                                │      SCORE /100       │
                                                └──────────┬───────────┘
                                                           │
                                                           │
                                                           │ besoin supplémentaire
                                                           ▼
                                                ╔══════════════════════╗
                                                ║      PARTIE 2        ║
                                                ║ DONNÉES PRIVÉES /    ║
                                                ║ PAYANTES ACQUISES    ║
                                                ║       PAR NOUS       ║
                                                ╚══════════╤═══════════╝
                                                           │
                                                           ▼
                                                ┌──────────────────────┐
                                                │  DONNÉES ENRICHIES   │
                                                └──────────┬───────────┘
                                                           ▼
                                                ┌──────────────────────┐
                                                │       ANALYSE         │
                                                └──────────┬───────────┘
                                                           ▼
                                                ┌──────────────────────┐
                                                │      SCORE /100       │
                                                └──────────┬───────────┘
                                                           │
                                                           │ besoin de données
                                                           │ difficiles
                                                           ▼
                                                ╔══════════════════════╗
                                                ║      PARTIE 3        ║
                                                ║ DONNÉES DIFFICILES   ║
                                                ║ D'ACCÈS /            ║
                                                ║ SOUS-TRAITÉES        ║
                                                ╚══════════╤═══════════╝
                                                           │
                                                           ▼
                                                ┌──────────────────────┐
                                                │  DONNÉES ENRICHIES   │
                                                └──────────┬───────────┘
                                                           ▼
                                                ┌──────────────────────┐
                                                │       ANALYSE         │
                                                └──────────┬───────────┘
                                                           ▼
                                                ┌──────────────────────┐
                                                │      SCORE /100       │
                                                └──────────────────────┘


══════════════════════════════════════════════════════════════════════════════════════════════════════

             PARTIE 4 — CONTINUOUS INTELLIGENCE
             ═══════════════════════════════════════════════════════════════════════════════════════

                    ▲                         ▲                         ▲
                    │                         │                         │
                    │ ACTIVABLE               │ ACTIVABLE               │ ACTIVABLE
                    │ depuis                  │ depuis                  │ depuis
                    │ PARTIE 1                │ PARTIE 2                │ PARTIE 3
                    │                         │                         │
                    └──────────────┐          │          ┌──────────────┘
                                   │          │          │
                                   ▼          ▼          ▼

                         ┌─────────────────────────────────────┐
                         │      CONTINUOUS INTELLIGENCE        │
                         │                                     │
                         │  MISE À JOUR DES DONNÉES            │
                         │              ↓                      │
                         │       NOUVELLE ANALYSE              │
                         │              ↓                      │
                         │       NOUVEAU SCORE /100            │
                         │              ↓                      │
                         │     ALERTES / RAPPORTS              │
                         │         PÉRIODIQUES                 │
                         │              │                      │
                         │              └──────────────┐       │
                         │                             │       │
                         │              ← BOUCLE DE SUIVI     │
                         └─────────────────────────────┼───────┘
                                                       │
                                                       │
                                  ┌────────────────────┴────────────────────┐
                                  │                                         │
                                  ▼                                         ▼
                           NIVEAU DE DONNÉES                         NOUVELLES DONNÉES
                           DU CLIENT CONSERVÉ                          À INTÉGRER
                            (N1 / N2 / N3)                                  │
                                  │                                         │
                                  └────────────────────┬────────────────────┘
                                                       │
                                                       ▼
                                                NOUVELLE ANALYSE
        


PARTIE 1 ────────┐
                  │
PARTIE 2 ────────┼──→ CONTINUOUS INTELLIGENCE
                  │
PARTIE 3 ────────┘



3. TRI / SÉLECTION DATA

« Parmi toutes les données qu'on a récupérées, lesquelles décide-t-on de conserver pour l'analyse de ce produit ? »


PARTIE 1
≈ 10 données / métriques sélectionnées
→ adaptées au produit et au besoin du client

PARTIE 2
≈ 15 données / métriques sélectionnées
→ + données permettant d'approfondir l'analyse

PARTIE 3
≈ 20 données / métriques sélectionnées
→ + données spécialisées / difficiles à obtenir

PARTIE 4
> 30 données / métriques potentielles
→ maximum exploitable selon le produit,
   les données disponibles et l'intérêt analytique


Le nombre un minimum cible, pas une règle rigide. 

Exemple très simple

Pour une huile cosmétique, les 10 données de Partie 1 pourraient être principalement autour de :

Produit
Prix
Devise
Unité
Date
Volume
Fournisseur
Origine
Qualité / grade
Conditions de livraison


Alors que pour de la farine, la sélection pourrait être différente :

Produit
Type de farine
Prix
Unité
Date
Volume
Fournisseur
Origine du blé
Taux de protéines
Qualité / classification


Donc on ne promet pas au client 10 champs universels.

On lui promet plutôt :

Partie 1 : un socle minimum d'environ 10 données pertinentes, sélectionnées spécifiquement pour le produit et l'objectif d'analyse.

Puis :

Partie 2 : environ 15 données pertinentes, avec enrichissement.

Puis :

Partie 3 : environ 20 données pertinentes, avec les informations supplémentaires que permettent les sources difficiles d'accès.

Et enfin :

Partie 4 : exploitation continue d'un ensemble de données pouvant dépasser 30 métriques lorsque le produit et les sources le permettent.

Et je garderais absolument ton idée de validation empirique : les chiffres 10 / 15 / 20 / +30 sont pour l'instant nos objectifs de conception, pas encore des vérités du produit. On devra tester sur plusieurs familles de produits pour voir si 30+ variables apportent réellement de la valeur ou si certaines deviennent redondantes.





4. QUALIFICATION DES DONNÉES 

La donnée est calculer par rapport à 4 critères : la qualité, la fraicheur, la provenance et la couverture. 

Pourquoi ces 4 critères ?

| Critère        | Question                                                            |
| -------------- | ------------------------------------------------------------------- |
| **Qualité**    | Est-ce que la donnée est correcte et exploitable ?                  |
| **Fraîcheur**  | Est-ce que la donnée représente encore le marché actuel ?           |
| **Provenance** | D'où vient-elle et comment a-t-elle été obtenue ?                   |
| **Couverture** | Est-ce qu'on a suffisamment de données pour représenter le marché ? |

Qualité — « Est-ce que la donnée est exploitable ? »

La qualité concerne le contenu même de l'observation.

Par exemple :

Prix : 7,20 €/kg
Produit : Cocoa Butter
Date : 2026-08-15
Quantité : 1 000 kg
Incoterm : FOB
Origine : Ghana
Qualité : Organic

C'est beaucoup plus exploitable que :

Cocoa Butter
7,20 €/kg

Pourquoi ?

Parce que le deuxième prix est impossible à comparer correctement.

Le premier peut être normalisé.

La qualité pourrait donc vérifier :

produit précisément identifié ;
unité ;
devise ;
quantité ;
date ;
origine ;
grade/qualité ;
Incoterm ;
lieu de livraison ;
MOQ ;
conditions commerciales ;
etc.

C'est là que le data cleaning + validation + normalisation intervient.  (à développer) 

Donc on ne récompense pas simplement « beaucoup d'informations ». On récompense la présence d'informations pertinentes et cohérentes permettant de contextualiser le prix.



Fraîcheur — « Est-ce que cette observation représente encore le marché ? »

C'est particulièrement important pour les matières premières.

Une observation de :

7,20 €/kg en janvier 2025

n'a pas la même valeur qu'une observation de :

7,20 €/kg en septembre 2026.

Mais attention : fraîcheur ≠ simplement âge de la donnée.

Une donnée vieille de six mois sur un marché très stable peut rester utile.

Une donnée vieille de six jours sur un marché extrêmement volatil peut déjà être dégradée.

Donc idéalement, le système pourra associer la fraîcheur à la dynamique du marché.

Conceptuellement :

Freshness Score
        ↓
âge de l'observation
        +
volatilité du marché
        +
fréquence de mise à jour

Plus tard, on pourrais même avoir une fonction de décroissance :

$$ Freshness(t)=e^{-\λt} $$

où λ dépendrait du type de marché.

Mais pas maintenant. Pour la première analyse, une classification simple suffit.

Exemple : 

< 30 jours      → très récent
30–90 jours     → récent
90–180 jours    → intermédiaire
> 180 jours     → ancien

Les seuils seront évidemment adaptés au produit. 


Provenance — « D'où vient la donnée et comment a-t-elle été obtenue ? »

Ici, on ne cherche pas encore à savoir si la donnée est bonne. On cherche à savoir quelle est son origine et quelle est la chaîne d'acquisition.

Par exemple, pour un prix de cacao à 7,20 €/kg :

7,20 €/kg
│
├── Source : fournisseur
├── Mode : devis transmis directement
├── Date : 15/08/2026
└── Intermédiaire : aucun

ou :

7,20 €/kg
│
├── Source : catalogue public
├── Mode : recherche web
├── Date de consultation : 04/09/2026
└── Prix affiché publiquement

ou encore :

7,20 €/kg
│
├── Source : base de données professionnelle
├── Mode : donnée acquise via abonnement
├── Date : 01/09/2026
└── Source spécialisée

Donc la provenance peut notamment renseigner :

source
type de source
mode d'acquisition
date d'obtention
chaîne de transmission éventuelle
source directe ou indirecte

On pourrait avoir par exemple :

CLIENT / TRANSACTION
FOURNISSEUR / DEVIS
RECHERCHE PUBLIQUE
CATALOGUE
MARKETPLACE
BASE DE DONNÉES
INDEX / MARCHÉ
EXPERT / AGENCE

Et c'est important pour notre système parce qu'une même information peut nous parvenir par plusieurs canaux.

La provenance décrit donc l'origine et le chemin de la donnée, pas sa qualité.

Une donnée provenant directement d'un fournisseur n'est pas automatiquement « vraie » simplement parce que sa provenance est excellente. Elle aura simplement une provenance clairement identifiée. La qualité sera évaluée séparément.



La couverture de l'information

Je la définirais ainsi :

La couverture mesure dans quelle mesure une information est suffisamment documentée par des sources pertinentes et indépendantes pour pouvoir être considérée comme représentative et fiable.

L'idée n'est donc pas simplement de compter les sources.

Prenons une observation :

Beurre de cacao — 7,20 €/kg — fournisseur X — Ghana — FOB — 1 000 kg — 15/08/2026

On peut avoir plusieurs éléments qui viennent renforcer cette information :

le devis directement fourni par le fournisseur ;
une transaction historique du client avec ce fournisseur ;
un catalogue ou tarif public du fournisseur ;
une base de données professionnelle ;
une autre source de marché donnant un niveau de prix comparable.

L'information est alors davantage couverte, parce qu'on ne dépend pas d'une seule observation isolée.

Mais il y a un point très important

5 sources ≠ automatiquement meilleure couverture que 2 sources.

Si les cinq sources reprennent toutes la même information provenant à l'origine du même fournisseur, on n'as en réalité pas cinq confirmations indépendantes.

Par exemple :

Site du fournisseur → marketplace → annuaire → article → autre catalogue

Si tout le monde a copié le même tarif fournisseur, cela ne constitue quasiment qu'une seule source primaire.

À l'inverse :

Devis fournisseur + facture historique client + base professionnelle

Là, on as des sources d'origines différentes qui peuvent réellement recouper l'information.

Donc, à terme, la couverture devra probablement tenir compte de trois choses :

Nombre de sources pertinentes + indépendance des sources + cohérence entre les sources.

Exemple concret

Imaginons que ton système ait :

Source	Information sur le prix
Devis fournisseur	7,20 €/kg
Historique client	7,35 €/kg
Base professionnelle	7,10 €/kg
Catalogue fournisseur	7,20 €/kg

on n'as pas simplement « 4 sources ».

Je peux constater que :

plusieurs sources indiquent un niveau proche ;
les sources ne sont pas toutes de même nature ;
certaines sont directement liées au fournisseur ;
certaines sont indépendantes.

L'information 7,20 €/kg devient donc beaucoup plus solide qu'un simple :

« Fournisseur X : 7,20 €/kg »

Et c'est là que la couverture devient intéressante pour le score

Je pourrais avoir deux fournisseurs avec une donnée de qualité similaire :

Fournisseur A

Prix = 7,20 €/kg
1 seule source : devis fournisseur

Fournisseur B

Prix = 7,20 €/kg
devis fournisseur + historique client + source professionnelle

La donnée de B est potentiellement mieux couverte.

Mais attention : cela ne signifie pas encore que B est meilleur que A. La couverture sert à déterminer le niveau de confiance que je peux accorder à l'information, pas à juger directement le fournisseur.


Partie 5 — Data Reliability

L'idée est que les 4 dimensions de qualification restent visibles séparément, puis soient agrégées dans un score final.


                 DATA À QUALIFIER
                       │
          ┌────────────┼────────────┐
          ▼            ▼            ▼
       QUALITÉ      FRAÎCHEUR    PROVENANCE    COUVERTURE
          │            │            │              │
        /100          /100         /100           /100
          │            │            │              │
          └────────────┴────────────┴──────────────┘
                              │
                              ▼
                    FORMULE D'AGRÉGATION
                              │
                              ▼
                   DATA RELIABILITY /100

à terme, les 4 critères ont vocation à être quantifiés.

Donc, pour une donnée donnée, le client pourrait voir par exemple :

| Dimension            |      Score |
| -------------------- | ---------: |
| Qualité              |     92/100 |
| Fraîcheur            |     81/100 |
| Provenance           |     95/100 |
| Couverture           |     74/100 |
| **Data Reliability** | **86/100** |


ex pour la provenance : 

SOURCE FOURNISSEUR
        ↓
   valeur élevée
        │
        ├────────┐
        │        │
CATALOGUE    MARKETPLACE
PUBLIC          etc.
        ↓        ↓
 valeurs différentes
        │
        └───────┬────────┘
                ▼
       PROVENANCE SCORE
             /100

| Provenance                                    | Valeur indicative |
| --------------------------------------------- | ----------------: |
| Transaction réelle / donnée client vérifiable |       Très élevée |
| Devis direct fournisseur                      |            Élevée |
| Donnée professionnelle spécialisée            |            Élevée |
| Donnée de marché structurée                   |            Élevée |
| Catalogue fournisseur public                  |           Moyenne |
| Marketplace                                   |          Variable |
| Estimation / source indirecte                 | Faible à variable |


Le point important est que le score final n'efface pas les quatre composantes.

Si le client voit 86/100, il doit pouvoir comprendre pourquoi :

« La donnée est très bien documentée et provient d'une source solide, mais elle est moins bien couverte par des sources indépendantes. »

C'est beaucoup plus intéressant commercialement qu'un simple « Reliability = 86 ».

Et surtout : les deux niveaux de quantification sont différents

On auras :

Niveau 1 — Score de chaque dimension

Chaque critère possède ses propres sous-critères et aboutit à un score /100.

Par exemple :

Qualité → plusieurs critères → 92/100

Fraîcheur → plusieurs critères → 81/100

Provenance → plusieurs critères → 95/100

Couverture → plusieurs critères → 74/100

Puis :

Niveau 2 — Data Reliability

Les quatre scores sont agrégés par une formule distincte pour obtenir :

Data Reliability = 86/100

Et je pense qu'il faut conserver cette distinction dans le modèle : les formules de calcul des quatre dimensions et la formule d'agrégation finale ne doivent pas être confondues.

Je ne cherches pas à décider moi-même de ce qui constitue une « bonne donnée métier ». Le client définit le besoin métier et les informations pertinentes pour son produit, tandis que je construis le système qui permet de mesurer objectivement la fiabilité des informations collectées.

Le client définit les exigences métier ; le système Data mesure et quantifie la fiabilité des informations au regard de ces exigences.

Et ça protège aussi notre modèle : on n'as pas besoin de créer une liste universelle de 50 critères valable pour l'huile, le cacao, la farine, les matières premières cosmétiques, etc. Le contenu métier s'adapte au client et au produit ; mon mécanisme de qualification, lui, reste structuré.


6. Normalisation Data


La qualification répond à :

« Est-ce que cette donnée est suffisamment fiable ? »

La normalisation répond à :

« Est-ce que je peux réellement comparer cette donnée avec les autres ? »

Ce sont deux problèmes différents.

Exemple simple

Je récupère :

Fournisseur A

7,20 €/kg — Cocoa Butter — FOB — Ghana — 1 000 kg

Fournisseur B

6 800 $/tonne — Cocoa Butter — CIF Rotterdam — 5 tonnes

Fournisseur C

7,50 €/kg — Cocoa Butter — EXW — 500 kg

On as potentiellement trois informations de qualité correcte.

Mais je ne peux pas encore mettre directement 7,20 / 6,80 / 7,50 dans un benchmark.

Il faut d'abord rendre les observations comparables.

Ce que fait la normalisation

Elle va essentiellement transformer des données hétérogènes en une structure commune.

Unités

Par exemple :

€/kg
$/tonne
€/tonne
£/lb

→ conversion vers une unité de référence.

Devise
EUR
USD
GBP
etc.

→ conversion selon une règle temporelle cohérente.

Produit

Un fournisseur peut écrire :

Cocoa Butter

Un autre :

Cocoa Butter Deodorized

Un autre :

Cacao Butter Organic

Il faut être capable de distinguer :

produit, qualité/grade, certification, etc., plutôt que de considérer automatiquement ces trois lignes comme identiques.

Quantité

Une offre à :

500 kg

n'est potentiellement pas comparable à :

20 tonnes

Le volume peut influencer le prix.

Conditions commerciales

Même chose pour :

Incoterm
lieu de livraison
délai
MOQ
conditions de paiement
etc.

Un prix FOB Ghana et un prix CIF Rotterdam ne représentent pas exactement la même chose.

Donc la normalisation ne veut pas dire « nettoyer les données »

On as déjà une partie Qualité dans Data Reliability où je fais notamment :

nettoyage → validation → cohérence → structure → unités → champs nécessaires

La normalisation va plus loin :

mettre les données dans une représentation commune permettant l'analyse comparative.

Il peut donc y avoir des opérations qui se ressemblent techniquement, mais leur objectif est différent.

Qualification :

Est-ce que cette donnée est exploitable et fiable ?

Normalisation :

Comment dois-je représenter cette donnée pour pouvoir la comparer aux autres ?


7. MARKET BENCHMARK

Le benchmark va donc construire une référence de marché à partir des données disponibles.

Par exemple, après normalisation :

| Fournisseur | Prix comparable |
| ----------- | --------------: |
| A           |       6,80 €/kg |
| B           |       7,10 €/kg |
| C           |       7,20 €/kg |
| D           |       7,40 €/kg |
| E           |       7,80 €/kg |
| **Client**  |   **8,10 €/kg** |


On peut alors dire que le fournisseur du client est au-dessus du niveau de prix observé sur le marché.

Mais le benchmark ne doit pas se limiter à une moyenne.

Ce que le benchmark doit chercher à mesurer

Pour chaque produit et chaque segment de marché, on peut construire plusieurs références :

niveau central du marché → médiane, moyenne selon le cas ;
dispersion → à quel point les prix sont éloignés les uns des autres ;
position du fournisseur → où se trouve son prix dans la distribution ;
écart au benchmark → différence entre le fournisseur et la référence ;
évolution du benchmark → comment le marché évolue dans le temps ;
éventuellement benchmark par segment → origine, qualité, volume, destination, conditions commerciales, etc.

Et c'est justement là que la normalisation devient fondamentale : on ne compare pas des prix qui correspondent à des réalités commerciales différentes.

Mais il y a une distinction importante

Le Market Benchmark ne dit pas encore :

« Le fournisseur est mauvais. »

Il dit :

« Voici comment son offre se positionne par rapport au marché observable. »

C'est une différence importante.

Un fournisseur peut être 15 % plus cher que le benchmark, mais avoir une qualité supérieure ou des conditions commerciales qui justifient cet écart.

C'est ensuite la Supplier Analysis qui va croiser ces différents éléments pour établir une analyse plus complète du fournisseur.

MARKET BENCHMARK
       │
       └── Où se situe mon fournisseur
           par rapport au marché ?
                    ↓
SUPPLIER ANALYSIS
       │
       └── Pourquoi se situe-t-il là ?
           Quel est son profil ?
           Quels sont ses avantages / risques ?
           Quelle est sa compétitivité globale ?


Et surtout, le benchmark sera dynamique

Comme mon système peut fonctionner avec de la Continuous Intelligence, le benchmark pourra être recalculé lorsque de nouvelles données arrivent.

Donc on peut avoir :

Benchmark actuel : 7,20 €/kg
Benchmark précédent : 6,95 €/kg
→ évolution du marché : +3,6 %

Et parallèlement :

Fournisseur client : 8,10 €/kg

Le système peut alors constater que le marché monte, mais que le fournisseur monte éventuellement plus vite ou moins vite que le marché.

C'est beaucoup plus intéressant qu'un simple comparatif ponctuel.



8. SUPPLIER ANALYSIS


Compétitivité

niveau de prix par rapport au marché ;
évolution de son positionnement ;
compétitivité selon les volumes/conditions ;
écarts avec les alternatives.

Performance

stabilité des prix ;
régularité des conditions ;
évolution historique ;
comportement par rapport au marché.

Risque fournisseur

dépendance ;
volatilité ;
anomalies ;
concentration ;
exposition à certaines conditions ou situations.

Fiabilité de l'information

on réutilise le Data Reliability /100 construit précédemment pour savoir à quel point les conclusions sur ce fournisseur sont solides.

On Imagine deux fournisseurs :

|                  | Fournisseur A | Fournisseur B |
| ---------------- | ------------: | ------------: |
| Prix observé     |        7,20 € |        6,90 € |
| Data Reliability |        95/100 |        52/100 |

Si on regardes uniquement le prix :

B semble clairement meilleur.

Mais mon système sait :

« Attention, l'information concernant B est beaucoup moins robuste. »

Donc la Supplier Analysis peut présenter :

B est moins cher selon les données disponibles, mais cette conclusion repose sur des données significativement moins fiables.



Avec une séparation fondamentale :

Data Reliability
→ « Peut-on faire confiance à cette information ? »

Market Benchmark
→ « Où se situe ce fournisseur par rapport au marché ? »

Supplier Analysis
→ « Quel est le profil, la performance, la compétitivité et le risque de ce fournisseur, compte tenu de sa position sur le marché ? »


9. Opportunity Engine

On sais maintenant :

comment se situe le fournisseur par rapport au marché ;
s’il est compétitif ;
comment il performe ;
quels sont ses risques ;
à quel point les données utilisées sont fiables.

L’Opportunity Engine pose une nouvelle question :

« Où est-ce que le client peut créer de la valeur ou réduire son risque ? »



Opportunité de prix

Le fournisseur est sensiblement au-dessus du benchmark → potentiel de négociation.

Opportunité de fournisseur

Une alternative présente un meilleur profil → possibilité de changer ou d'ajouter un fournisseur.

Opportunité de diversification

Le fournisseur actuel est bon mais la dépendance est trop importante → rechercher une alternative pour réduire l'exposition.

Opportunité de maintien

Le fournisseur est compétitif et performant → aucune action majeure nécessaire.

Opportunité liée au timing (relié à toutes les autres) 

Le marché évolue dans une direction favorable → moment potentiellement pertinent pour renégocier, acheter davantage ou attendre.

Le système observe l'évolution d'un prix ou d'une variable dans le temps.

Par exemple :

Prix fournisseur : 8,20 → 7,90 → 7,60 → 7,30 €/kg

On ne regarde donc plus seulement où est le prix aujourd'hui, mais dans quelle direction il évolue et à quelle vitesse.

Cela peut faire apparaître une opportunité :

Tendance baissière persistante → potentiel intérêt à attendre avant de renégocier / acheter.

Ou à l'inverse :

Tendance haussière persistante → intérêt potentiel à négocier rapidement ou sécuriser un prix.


Anticipation / estimation future

Et là, l' exemple est encore plus intéressant.

Le système constate :

« Le prix de cette matière chez ce fournisseur diminue continuellement depuis plusieurs mois. »

Je peux alors utiliser l'historique, la dynamique du marché et ensuite des modèles statistiques pour estimer des scénarios futurs.

Par exemple :

Prix actuel : 7,30 €/kg
Scénario central à 3 mois : 6,80 €/kg
Intervalle possible : 6,30–7,40 €/kg

L'Opportunity Engine peut alors détecter :

Opportunité potentielle de timing : évolution anticipée favorable.

Et cela peut déboucher sur plusieurs stratégies :

Renégocier maintenant
si le marché est susceptible de repartir à la hausse.

Attendre
si le marché semble continuer à baisser.

Fixer un prix futur / contractualiser
si l'estimation montre une fenêtre intéressante pour sécuriser les conditions.

Augmenter ou réduire les volumes
selon le contexte.



Et c’est là que la Continuous Intelligence prend vraiment sa place dans mon architecture.

L'opportunité liée au timing n'est pas simplement :

« une cinquième catégorie d'opportunité ».

C'est plutôt une dimension temporelle qui peut modifier toutes les autres opportunités.



10. RECOMMANDATION finale

Je ne veux pas donner au client :

« Renégociez. »
ou
« Ne renégociez pas. »

Mias lui donner une décision accompagnée de son niveau d’incertitude et de scénarios quantifiés.


Exemple

Le système détecte une tendance baissière sur une matière première.

Au lieu de :

« Le prix va probablement baisser. »

Tu pourrais arriver à quelque chose comme :

Prix actuel : 7,40 €/kg
Prix médian estimé à 3 mois : 6,95 €/kg
Probabilité que le prix soit inférieur à 7,00 €/kg dans 3 mois : 68 %
Probabilité qu'il dépasse 7,80 €/kg : 12 %

Là, le client peut réellement raisonner en termes de risque / rendement / timing 


Simmulation de monte carlo :

générer beaucoup de trajectoires/scénarios possibles à partir des distributions et incertitudes observées.

Donc :

Prix futur
   │
   ├── scénario défavorable
   ├── scénario central
   ├── scénario favorable
   └── distribution complète


Et non pas prétendre connaître un prix futur unique.


Inférence bayésienne

Elle apporte une autre logique :

chaque nouvelle information met à jour mon estimation.

Puis arrivent :

nouveaux prix fournisseur ;
nouvelles transactions ;
nouvelles données de marché ;
changement de tendance ;
nouvelles informations qualitatives.

Le modèle met à jour ses croyances/probabilités.

Donc avec la Continuous Intelligence :


Nouvelle donnée
      ↓
Mise à jour du modèle
      ↓
Nouvelles probabilités
      ↓
Nouveaux scénarios
      ↓
Opportunity Engine mis à jour
      ↓
Recommandation actualisée

Je ne promet pas :

« Nous savons ce qui va arriver. »

Mais quelque chose de plus sérieux :

« Nous quantifions les scénarios possibles, leur probabilité et leur évolution à mesure que de nouvelles données apparaissent. »

Et ça colle parfaitement à mon architecture :

Data Reliability → quelle confiance dans les données ?
Market Benchmark → où sommes-nous par rapport au marché ?
Supplier Analysis → quel est le profil du fournisseur ?
Opportunity Engine → où sont les opportunités ?
Recommendation → quelles sont les probabilités et scénarios associés ? Et quelle action paraît la plus rationnelle compte tenu de ces résultats ?


