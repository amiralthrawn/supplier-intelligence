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
Le système

Combine les deux.

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
que certains clients paient moins cher ;
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
Données publiques recherchées par toi
        ↓
PREMIÈRE ANALYSE

Je peux aller chercher :

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



Fraîcheur — « Est-ce que cette observation représente encore le marché ? »

C'est particulièrement important pour les matières premières.

Une observation de :

7,20 €/kg en janvier 2025

n'a pas la même valeur qu'une observation de :

7,20 €/kg en septembre 2026.

Mais attention : fraîcheur ≠ simplement âge de la donnée.

Une donnée vieille de six mois sur un marché très stable peut rester utile.

Une donnée vieille de six jours sur un marché extrêmement volatil peut déjà être dégradée.

Donc idéalement, ton système pourra associer la fraîcheur à la dynamique du marché.

Conceptuellement :

Freshness Score
        ↓
âge de l'observation
        +
volatilité du marché
        +
fréquence de mise à jour

Plus tard, tu pourrais même avoir une fonction de décroissance :

$$ Freshness(t)=e^{-\λt} $$

où λ dépendrait du type de marché.

Mais pas maintenant. Pour la première analyse, une classification simple suffit.

Exemple : 

< 30 jours      → très récent
30–90 jours     → récent
90–180 jours    → intermédiaire
> 180 jours     → ancien

Les seuils seront évidemment adaptés au produit. 


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
                              │ pertinentes pour l'offre  │
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
que certains clients paient moins cher ;
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
Données publiques recherchées par toi
        ↓
PREMIÈRE ANALYSE

Je peux aller chercher :

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

Tu peux donc les acheter directement.

Et enfin :

F — Données nécessitant une collecte sous-traitée

Lorsque la collecte nécessite :

sourcing spécialisé ;
appels ;
demandes de devis ;
vérifications ;
expertise sectorielle ;
enquête de marché ;

tu peux faire intervenir une agence, un expert ou un prestataire spécialisé.

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









      DONNÉE COLLECTÉE
                     ↓
        ┌────────────┼────────────┐
        ↓            ↓            ↓
     QUALITÉ     FRAÎCHEUR    PROVENANCE
                                   +
                               COUVERTURE
                     ↓
              TEST DE FIABILITÉ
                     ↓
             DONNÉE QUALIFIÉE
