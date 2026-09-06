# supplier-intelligence
Supplier and procurement intelligence system for wholesale businesses

1. Problème identifié

Un grossiste qui dépend de fournisseurs historiques (fixe) dispose d'une excellente connaissance de ses propres fournisseurs, mais d'une visibilité insuffisante sur la compétitivité réelle du marché.

Origine du projet
L'idée est née à la croisée de deux expériences distinctes menées à la même période (début 2026) :
Un travail sur un projet d'arbitrage sur les marchés de commodities, en particulier sur la volatilité des prix du pétrole depuis le début de l'année 2026 — une volatilité qui a généré de nombreuses opportunités de marché.
En parallèle, dans le cadre d'une recherche d'alternance, l'exploration de plusieurs sites de grossistes travaillant dans l'import-export, où il est apparu que plusieurs grossistes ne dépendaient que d'un seul fournisseur par produit.
L'idée : transposer la logique de compétitivité de marché et de vision globale (utilisée sur les marchés de commodities comme le pétrole) au monde de l'import-export, sous forme de service destiné aux grossistes — en particulier ceux dépendants d'un seul fournisseur par produit.

Les 6 risques lié au problème :


Point clé : ces risques ne sont pas de simples signaux à remonter, ils sont quantifiables à partir de données puis transformables en décisions. C'est là que se situe la vraie valeur ajoutée du système

Risque prix — le fournisseur augmente ses prix alors que le marché comparable évolue dans le sens inverse. Exemple : en janvier, fournisseur à 7,00 €/kg contre un benchmark à 7,10 €/kg. En avril, fournisseur à 7,60 €/kg contre un benchmark à 6,90 €/kg. Le problème n'est pas que le fournisseur devient "cher" en absolu, c'est que son positionnement se détériore relativement au marché (+8,6 % fournisseur vs −2,8 % marché) — ce qui peut alimenter une opportunité de renégociation ou de recherche d'alternative.

Risque de dépendance — le grossiste dépend fortement d'un fournisseur sans alternative suffisamment identifiée. Exemple : un grossiste achète 80 % de son beurre de cacao auprès d'un seul fournisseur (origine particulière, délais importants, aucune alternative qualifiée disponible immédiatement). Même compétitif aujourd'hui, le grossiste reste vulnérable à une hausse de prix, un problème de production, une rupture ou une dégradation des délais. Le système ne dit pas "quittez ce fournisseur", mais plutôt : "le maintenir peut être rationnel économiquement, mais identifier une seconde source réduirait l'exposition."

Risque logistique — le prix n'est pas nécessairement le problème. Exemple : fournisseur A à 7,00 €/kg mais délai passé de 15 à 28 jours, coût transport +12 %, taux de retard passé de 3 % à 14 %. Fournisseur B à 7,15 €/kg mais délai stable de 12 jours, transport stable, peu de retards. A paraît moins cher sur le prix seul, mais l'avantage peut disparaître une fois les conditions logistiques intégrées — d'où l'importance de la normalisation et des conditions commerciales.

Risque qualité — le fournisseur reste compétitif en prix mais la qualité devient moins régulière. Exemple : conformité qualité passée de 98 % à 89 % sur certaines périodes/origines, sans changement de prix — générant lots refusés, retraitement, pertes, retours. Le système peut chercher une relation temporelle (changement d'origine → évolution qualité → hausse des anomalies), ce qui est plus riche qu'un simple taux de défaut brut.

Risque commercial — le fournisseur est compétitif en prix facial mais moins intéressant dans les conditions réelles de transaction. Exemple : fournisseur A à 7,00 €/kg avec MOQ de 10 tonnes et paiement à 30 jours vs fournisseur B à 7,20 €/kg avec MOQ de 1 tonne et disponibilité immédiate. Pour un besoin de 2 tonnes, les 20 centimes d'écart ne racontent pas toute l'histoire — A peut être économiquement moins intéressant dans ce contexte. Le Benchmark doit comparer des conditions comparables, pas seulement des prix.

Risque d'opportunité — probablement le point le plus porteur de valeur. Ce n'est pas "quelque chose de mauvais va arriver", mais "quelque chose d'intéressant est disponible, mais le client ne le voit pas". Exemple : un grossiste travaille depuis 3 ans avec A à 7,40 €/kg. Une nouvelle source B apparaît sur le marché observable à 6,90 €/kg, mais n'est pas connue du grossiste. Le système détecte l'écart (A = 7,40 €, benchmark = 7,00 €, B = 6,90 €) et identifie une opportunité potentielle — mais l'analyse automatisé doit ensuite qualifier cette opportunité (qualité, MOQ, Incoterm, origine, délais, fiabilité des données de B), pas simplement repérer le prix le plus bas.

Le timing, en dimension transversale à ces risques : une opportunité peut être plus intéressante demain qu'aujourd'hui, ou l'inverse. Exemple : fournisseur A à 7,40 €/kg, marché à 7,20 €/kg, mais tendance baissière observée sur plusieurs mois → scénario central à 3 mois estimé à 6,85 €/kg, probabilité de passer sous 7,00 € à 68 %. Ce n'est pas une prédiction certaine, c'est une représentation probabiliste de l'incertitude, qui peut changer la décision : attendre si le marché risque de baisser, sécuriser un volume si le marché risque de monter, répartir les achats en cas de forte incertitude. 

Vision produit :
Le système ne se limite pas à dire « vous payez 7,40 € alors que le marché est à 7,00 € » — un bon acheteur peut éventuellement le découvrir seul. L'ambition est de pouvoir dire, progressivement : « Voici votre position actuelle. Voici pourquoi elle est ainsi. Voici les risques auxquels vous êtes exposé. Voici les opportunités détectées. Et compte tenu de l'évolution observée et des scénarios possibles, voici les décisions envisageables et leurs conséquences. »
Ce passage d'un outil de reporting à un véritable outil d'aide à la décision achats implique une exigence de rigueur méthodologique croissante sur le Benchmark : plus on avance vers la décision et la prédiction, plus le coût d'une donnée ou d'une méthode erronée augmente.



2. Fonctionnement global
Répartition des rôles

Le porteur du projet ne peut pas devenir expert simultanément de chaque marché (pétrole, cacao, kaolin, huiles végétales, farine, actifs cosmétiques, etc.). Son rôle est circonscrit à Data / Intelligence : pipeline de données, nettoyage, normalisation, comparaison, statistiques, modèles, scoring, détection d'anomalies, simulation, dashboard/reporting.

En complément, le rôle Procurement / Commodity est porté côté grossiste : soit par un spécialiste data interne au grossiste, soit par le grossiste lui-même s'il gère cette fonction personnellement. Ce n'est pas un expert externe mobilisé par le porteur du projet — c'est bien un interlocuteur qui appartient à l'organisation du client, et qui apporte la connaissance des fournisseurs, la qualité acceptable, les contraintes réglementaires, les spécifications techniques, la saisonnalité, la réalité du marché, les fournisseurs réellement crédibles, et les informations difficiles à obtenir automatiquement.

Le système combine les deux — jugé plus crédible qu'un système prétendant tout savoir et tout régler automatiquement seul.

En dehors de ces points de contact (acquisition et qualification des données, voir ci-dessous), l'ensemble du pipeline (tri, normalisation, benchmark, supplier analysis, opportunity engine, recommandation) est réalisé  par le porteur du projet.

Les 4 étapes de la relation client

Étape 0 — Prise de contact / démonstration (avant signature, gratuite)

Le client transmet un minimum d'informations. Le porteur du projet les compare à des informations d'autres fournisseurs et produit un premier résultat de démonstration, sur 3 à 4 données par fournisseur. Charge de travail réduite, niveau de fiabilité volontairement plus faible. Objectif du message : « l'an dernier, vous auriez pu... ». Cette démonstration sert de base à la décision de signer ou non.

Palier I — Premier projet réel (une fois signé)

Ressemble à la démo mais avec le processus complet exécuté (les 10 étapes en détail), sur environ 10 métriques par fournisseur. Résultat : un chiffrage quantitatif des choix que le client peut prendre dès maintenant, avec les implications de chaque choix.

Palier II — Enrichissement (si le client veut plus de certitude)

Si le client souhaite augmenter le taux de fiabilité de l'analyse ou couvrir des données non prises en compte précédemment : passage à 15-20 données, potentiellement incluant des données payantes.

Palier III — Le plus premium

Plus de 30 données : l'ensemble des données disponibles sur le produit, avec un appel à des professionnels du marché pour obtenir des données supplémentaires — possible volet de sous-traitance à ce niveau.

Continuous Intelligence — option transversale, pas une 5ᵉ étape

Accessible dès le Palier I, indépendamment du niveau de données choisi. Le client signe un contrat pour recevoir une analyse à la fréquence souhaitée (mensuelle, trimestrielle...), avec le volume de données de son choix (10, 20 ou 30+) à chaque nouvelle analyse.

Ce que le client transmet (une fois engagé, Paliers I à III)
Le périmètre de l'analyse — produits et fournisseurs respectifs soumis à l'analyse.
Les données concomitantes à l'analyse — prix d'achat, volumes, historique, délais, qualité, transport, conditions de paiement, pays d'origine, etc.
Les données secondaires, variables selon le produit — non indispensables à l'analyse de base mais potentiellement précieuses selon le contexte : origine de production, principal importateur du produit en France, écarts de prix du fournisseur selon les clients, connaissance d'autres fournisseurs potentiels, etc. Liste amenée à évoluer produit par produit.
Une hiérarchie de préférences propre au produit — le client (ou son spécialiste Procurement/Commodity) classe ce qui compte le plus dans l'engagement avec un fournisseur, du plus important au moins important (ex. qualité dominante pour la farine, prix dominant pour une huile). Configure directement la pondération du scoring.
Des données additionnelles à la demande — dans la limite du volume de métriques du Palier souscrit.

Ce que le prestataire apporte en plus, selon le Palier
Palier I : donnée multi-fournisseurs que le client n'a probablement pas le temps de rechercher lui-même (Catégorie D).
Palier II : donnée plus difficile à obtenir, nécessitant acquisition, potentiellement payante (Catégorie E).
Palier III : donnée obtenue via des spécialistes externes — agence de sourcing, expert marché, base spécialisée (Catégorie F).

Point de méthode déjà posé : une observation indirecte (ex. "Concurrent X achète chez fournisseur Y") ne permet jamais de conclure sur un prix accessible ("Y peut proposer 7,20 €/kg"), seulement qu'il s'agit d'une source potentielle à investiguer.

Restitution du résultat

Rapport (docx, potentiellement accompagné d'un volet Excel — à trancher), volontairement simple et brut. L'effort est mis sur le cœur du produit plutôt que sur l'automatisation ou la mise en forme de la restitution, jugée secondaire à ce stade.

Délai de livraison

Aucun délai encore défini — première expérience du porteur de projet dans cet exercice. Seul engagement actuel : livraison la plus rapide possible, plafond indicatif de moins d'un mois.



3. Architecture du produit
Principe général

L'architecture repose sur la combinaison de quatre couches indépendantes qui se superposent sans se confondre :

Étapes (1 à 10) — l'axe technique : le pipeline de traitement, toujours parcouru dans le même ordre.
Catégories (A à F) — l'axe des sources : d'où vient chaque donnée injectée dans le pipeline.
Paliers (I à IV) — l'axe commercial : combien de données sont traitées, et donc jusqu'où le pipeline est "rempli".
Continuous Intelligence — l'axe temporel : rejoue le pipeline périodiquement sur des données mises à jour.

Le Data Engine est le nom donné au sous-système qui exécute les Étapes 5 à 9 (Data Reliability → Normalisation → Market Benchmark → Supplier Analysis → Opportunity Engine) — le cœur calculatoire du produit, une fois les données acquises, triées et qualifiées.

Schéma d'ensemble

                               GROSSISTE
                                   │
                                   ▼
                  DONNÉES INITIALEMENT DISPONIBLES
                                   │
                  ┌────────────────┴────────────────┐
                  ▼                                 ▼
          DONNÉES FOURNIES                 DONNÉES RECHERCHÉES
           PAR LE CLIENT                        PAR NOUS
                  │                                 │
                  └────────────────┬────────────────┘
                                   ▼
                      ÉTAPE 0 — PREMIÈRE ANALYSE (démo)
                                   │
                                   ▼
                         PRÉSENTATION AU CLIENT
                                   │
                  ┌────────────────┴────────────────┐
                  ▼                                 ▼
           N'ACCEPTE PAS                        ACCEPTE
                  │                                 │
                  ▼                                 ▼
           FIN DE MISSION                   ╔═══════════════╗
                                            ║   PALIER I    ║
                                            ╚═══════╤═══════╝
                                                    │
                                     ┌──────────────┴──────────────┐
                                     ▼                             ▼
                          SPÉCIALISTE DATA /                DONNÉES SUPPL.
                          PROCUREMENT DU CLIENT              FOURNISSEURS/MARCHÉ
                                     └──────────────┬──────────────┘
                                                    ▼
                                          ÉTAPE 2 — ACQUISITION
                                          (Catégories A à D)
                                                    │
                                                    ▼
                                          ÉTAPE 3 — SÉLECTION
                                          (≈10 métriques)
                                                    │
                                                    ▼
                                    ┌───────────────────────────┐
                                    │        DATA ENGINE         │
                                    │        (Étapes 5-9)        │
                                    └──────────────┬──────────────┘
                                                   ▼
                                        ÉTAPE 10 — RECOMMANDATION
                                                   │
                                        besoin supplémentaire ?
                                                   ▼
                                            ╔═══════════════╗
                                            ║  PALIER II    ║
                                            ║ (Catégorie E) ║
                                            ╚═══════╤═══════╝
                                                    ▼
                                        ≈15-20 métriques → Data Engine → Recommandation
                                                   │
                                        besoin de données difficiles ?
                                                    ▼
                                            ╔═══════════════╗
                                            ║  PALIER III   ║
                                            ║ (Catégorie F) ║
                                            ╚═══════╤═══════╝
                                                    ▼
                                        >30 métriques → Data Engine → Recommandation

        PALIER I ──┐
        PALIER II ─┼──→  activable vers  ──→  CONTINUOUS INTELLIGENCE (Palier IV)
        PALIER III ┘

Logique de montée en charge (Paliers)

Chaque Palier ne repart pas de zéro : les données enrichies s'accumulent (Palier II = Palier I + nouvelles données de Catégorie E, Palier III = Palier II + nouvelles données de Catégorie F). Le Data Engine est retraversé à chaque Palier avec le jeu de données mis à jour, produisant une nouvelle Recommandation à chaque fois.

Recommandation : recalcul complet du Data Reliability à chaque Palier, pas incrémental — au moins pour cette première version. Trois raisons :
Défendabilité face au client. Si le score de fiabilité passe de 82 à 87 après enrichissement, je dois pouvoir expliquer pourquoi de façon limpide. Un recalcul complet se justifie simplement ("recalculé sur l'ensemble des données disponibles"). Un recalcul incrémental oblige à justifier une pondération ancien/nouveau score que tu n'as pas encore conçue — c'est un paramètre arbitraire de plus à défendre, alors que je cherche justement à réduire l'ambiguïté méthodologique.

Cohérence avec : "plus tu vas vers la décision et la prédiction, plus le coût d'une mauvaise donnée ou d'une mauvaise méthode augmente". Un recalcul incrémental introduit un risque de dérive silencieuse (une erreur ancienne pèse indéfiniment, même diluée) — un recalcul complet repart d'une base saine à chaque fois.
Simplicité d'implémentation pour un lancement terrain où je suis seul à tout exécuter manuellement — recalculer entièrement est mécaniquement plus simple qu'entretenir deux logiques de calcul (initial vs incrémental).
Le recalcul incrémental garde un intérêt réel — coût de calcul plus faible, utile si un jour le produit tourne à grande échelle et en automatique — mais ce n'est pas le problème du lancement terrain. Je le mets en "piste d'optimisation future", pas en choix d'architecture actuel.
Je fige donc ça comme choix par défaut (à confirmer/infirmer une fois testé en conditions réelles, comme tu le proposais), et je note la sélection de métriques comme non strictement additive : le passage à un Palier supérieur peut remplacer des données jugées trop marginales, ou répondre à une nouvelle analyse demandée par le client sans certaines métriques.

Architecture du produit — mise à jour finale des deux points ouverts :
Data Reliability Score : recalculé intégralement à chaque Palier, sur l'ensemble cumulé des données disponibles à ce stade (choix par défaut, à valider empiriquement — le recalcul incrémental reste une piste d'optimisation future).

Sélection des métriques (Étape 3) : non strictement additive — une donnée retenue à un Palier peut être écartée au Palier suivant si elle s'avère marginale, ou à la demande du client pour une nouvelle analyse.



4. Acquisition des données (Étape 2)
Les 6 catégories de sources

<img width="731" height="707" alt="Capture d’écran 2026-09-06 062244" src="https://github.com/user-attachments/assets/e7b09406-4149-4297-b52f-5ac20a096a50" />


Correspondance avec les Paliers (déjà établie en section 2)
Palier I mobilise les Catégories A, B, C et D — c'est la combinaison qui produit la première analyse complète (~10 métriques).
Palier II ajoute la Catégorie E.
Palier III ajoute la Catégorie F.
Règle épistémologique fondamentale de l'acquisition

Une observation indirecte ne vaut jamais une donnée directement exploitable. Exemple : si on observe que "Concurrent X achète chez fournisseur Y", on ne peut pas conclure "fournisseur Y peut proposer 7,20 €/kg au client" — on peut seulement conclure "fournisseur Y constitue une source potentielle à investiguer".

Cette règle a une implication directe sur l'architecture : toute donnée acquise par inférence ou observation indirecte (typiquement en Catégorie B et D) doit être marquée comme non confirmée jusqu'à passage par l'Étape 4 (Qualification) — elle ne peut pas être traitée avec le même niveau de confiance qu'une donnée directement transmise ou vérifiée par contact (Catégorie A, C, F).



5. Sélection des données (Étape 3)
Question centrale

« Parmi toutes les données récupérées, lesquelles décide-t-on de conserver pour l'analyse de ce produit ? »

Volumes cibles par Palier
<img width="729" height="267" alt="Capture d&#39;écran 2026-09-06 063149" src="https://github.com/user-attachments/assets/f8fac228-2b9f-498a-98a8-4aa38b465e1e" />

Ces volumes sont des objectifs de conception, pas des règles rigides — un minimum cible. Point de méthode assumé : ces chiffres (10/15/20/30+) devront être validés empiriquement sur plusieurs familles de produits, pour vérifier si un volume élevé de métriques apporte réellement de la valeur ou si certaines deviennent redondantes au-delà d'un certain seuil.

Principe : la sélection n'est jamais universelle

Le socle de 10 données du Palier I n'est pas un jeu de champs fixe et universel — il varie selon le produit. Exemple : pour une huile cosmétique, le socle porte principalement sur Produit, Prix, Devise, Unité, Date, Volume, Fournisseur, Origine, Qualité/grade, Conditions de livraison. Pour de la farine, la sélection change : Produit, Type de farine, Prix, Unité, Date, Volume, Fournisseur, Origine du blé, Taux de protéines, Qualité/classification.

Autrement dit, le produit ne promet jamais "10 champs universels" — il promet une méthodologie de sélection adaptée à chaque produit et à l'objectif d'analyse du client.

Cohérence avec la décision d'architecture (section 3)

Comme tranché en section 3, la sélection n'est pas strictement additive : une donnée retenue au Palier I peut être écartée au Palier II ou III si elle s'avère marginale à l'usage, ou si le client demande une nouvelle analyse sans certaines métriques.

Socle générique de départ (Palier I, ≈10 données)
<img width="727" height="430" alt="Capture d&#39;écran 2026-09-06 063613" src="https://github.com/user-attachments/assets/f2479479-4938-4a75-ac15-caafc5ce751d" />

Ce socle sert de point de départ standard, que le porteur du projet adapte ensuite au produit analysé — certains champs génériques (ex. Origine, Qualité/grade) sont remplacés par leurs équivalents plus précis et pertinents pour le produit (ex. pour la farine : Origine → Origine du blé ; Qualité/grade → Taux de protéines + Qualité/classification).

Qui décide de la sélection

C'est donc bien le porteur du projet, à partir de ce socle générique et de son jugement de data, qui fixe la sélection finale pour un produit donné — la hiérarchie de préférences transmise par le client (section 2) intervient, elle, au niveau de la pondération du scoring, pas au niveau du choix des champs eux-mêmes.

(le reste de la section — volumes cibles par Palier, principe de non-universalité, non-additivité entre Paliers — reste inchangé, voir version précédente)



6. Qualification des données (Étape 4)

Chaque donnée est évaluée sur 4 critères indépendants, chacun noté /100, avant d'être agrégée en Data Reliability (Étape 5) :
<img width="725" height="213" alt="Capture d&#39;écran 2026-09-06 063907" src="https://github.com/user-attachments/assets/b2bd37ec-19c5-4520-9b0b-3c4bf561b979" />

Qualité

Concerne le contenu même de l'observation — pas si le prix est bon ou mauvais, mais s'il est correctement contextualisé pour être comparable. Exemple : "Prix : 7,20 €/kg, Produit : Cocoa Butter, Date : 2026-08-15, Quantité : 1000 kg, Incoterm : FOB, Origine : Ghana, Qualité : Organic" est exploitable et normalisable. À l'inverse, "Cocoa Butter — 7,20 €/kg" seul est impossible à comparer correctement — il manque le contexte.

Champs vérifiés : produit précisément identifié, unité, devise, quantité, date, origine, grade/qualité, Incoterm, lieu de livraison, MOQ, conditions commerciales.

Principe : on ne récompense pas "beaucoup d'informations", mais la présence d'informations pertinentes et cohérentes qui permettent de contextualiser le prix.

Fraîcheur

Répond à : "cette observation représente-t-elle encore le marché ?" — mais fraîcheur ≠ simple âge de la donnée. Une donnée de 6 mois sur un marché stable peut rester utile ; une donnée de 6 jours sur un marché très volatil peut déjà être dégradée.

Composition conceptuelle : âge de l'observation + volatilité du marché + fréquence de mise à jour.

Pour la première version, une classification simple suffit (seuils à adapter par produit) :
<img width="729" height="195" alt="Capture d&#39;écran 2026-09-06 064110" src="https://github.com/user-attachments/assets/bddfa0bd-682e-4cc9-807d-c888ee7379f3" />

Piste future (non prioritaire) : une fonction de décroissance continue type Freshness(t) = e^(−λt), où λ dépendrait du type de marché — mais pas nécessaire pour la première analyse.

Provenance

Répond à : "d'où vient la donnée et comment a-t-elle été obtenue ?" — ici, on ne juge pas encore si la donnée est bonne, seulement son origine et sa chaîne d'acquisition.

Types de source envisagés : Client/Transaction, Fournisseur/Devis, Recherche publique, Catalogue, Marketplace, Base de données, Index/Marché, Expert/Agence.

Point important : la provenance décrit l'origine et le chemin de la donnée, pas sa qualité. Une donnée directement transmise par un fournisseur n'est pas automatiquement "vraie" du simple fait d'avoir une provenance bien identifiée — sa qualité est évaluée séparément, par le critère Qualité.

Couverture

"L'information est-elle suffisamment documentée par des sources pertinentes et indépendantes pour être considérée comme représentative et fiable ?"

Point clé : ce n'est pas un simple comptage de sources. Cinq sources qui recopient toutes la même information primaire (ex. le tarif d'un fournisseur repris par un site, une marketplace, un annuaire, un article) ne constituent quasiment qu'une seule source primaire. À l'inverse, un devis fournisseur + une facture historique client + une base professionnelle sont des origines réellement différentes qui peuvent se recouper.

La couverture tient donc compte de trois éléments combinés : nombre de sources pertinentes + indépendance des sources + cohérence entre elles.

Exemple : Fournisseur A à 7,20 €/kg avec une seule source (devis fournisseur) vs Fournisseur B à 7,20 €/kg avec trois sources indépendantes (devis + historique client + base professionnelle) — B est potentiellement mieux couvert. Mais attention : ça ne veut pas dire que B est "meilleur" que A commercialement — la couverture sert à déterminer le niveau de confiance accordé à l'information, pas à juger directement le fournisseur.


7. Data Reliability (Étape 5)
Principe d'agrégation à deux niveaux

Le point essentiel : le score final n'efface jamais les quatre composantes. Le client doit toujours pouvoir comprendre pourquoi il obtient un score donné, pas juste le chiffre brut.

Niveau 1 — Score de chaque dimension : chaque critère de qualification (Qualité, Fraîcheur, Provenance, Couverture) possède ses propres sous-critères et aboutit à un score /100 indépendant.

Niveau 2 — Data Reliability : les quatre scores sont agrégés par une formule distincte pour produire le score final.

                      DATA À QUALIFIER
                             │
          ┌────────────┼────────────┬──────────────┐
          ▼            ▼            ▼              ▼
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

Exemple de restitution client (les 4 sous-scores restent toujours visibles à côté du score agrégé) :
<img width="725" height="233" alt="Capture d&#39;écran 2026-09-06 064500" src="https://github.com/user-attachments/assets/cf2a6652-c219-4d8c-9696-cf2716d47ada" />

Interprétation attendue côté client : « la donnée est très bien documentée et provient d'une source solide, mais elle est moins bien couverte par des sources indépendantes » — une explication qualitative, pas juste "Reliability = 86".

Barème indicatif par exemple pour la Provenance

<img width="726" height="311" alt="Capture d&#39;écran 2026-09-06 064610" src="https://github.com/user-attachments/assets/8c6e3698-92fe-4c92-9237-f5418b492bdd" />

Séparation stricte entre les deux niveaux de formule

Les formules de calcul des 4 dimensions et la formule d'agrégation finale ne doivent jamais être confondues dans le modèle — ce sont deux mécanismes distincts, qui pourront évoluer indépendamment l'un de l'autre.

Répartition du jugement métier vs mesure objective

Principe fondamental, déjà énoncé implicitement en section 1 : le porteur du projet ne décide pas lui-même ce qui constitue "une bonne donnée métier" — le client définit les exigences métier (les informations pertinentes pour son produit), tandis que le système mesure objectivement la fiabilité des informations collectées au regard de ces exigences.

Cette séparation protège le modèle : pas besoin de bâtir une liste universelle de critères valable pour l'huile, le cacao, la farine et les actifs cosmétiques à la fois. Le contenu métier s'adapte au client et au produit ; le mécanisme de qualification, lui, reste structurellement identique.


8. Normalisation (Étape 6)
Distinction avec la Qualification

La Qualification répond à : « cette donnée est-elle suffisamment fiable ? »
La Normalisation répond à : « puis-je réellement comparer cette donnée avec les autres ? »

Ce sont deux questions différentes, même si certaines opérations techniques peuvent se ressembler (nettoyage, structuration). La Qualification (via le critère Qualité) fait déjà : nettoyage → validation → cohérence → structure → unités → champs nécessaires. La Normalisation va plus loin : elle met les données dans une représentation commune permettant l'analyse comparative — ce n'est donc pas un simple "nettoyage" redondant avec l'Étape 4.

Exemple révélateur du problème

Trois observations de qualité correcte, mais non directement comparables en l'état :
<img width="724" height="158" alt="Capture d&#39;écran 2026-09-06 065007" src="https://github.com/user-attachments/assets/0b08906b-9603-48e2-a5d4-56549619840b" />

Impossible de mettre directement 7,20 / 6,80 / 7,50 dans un benchmark sans d'abord rendre ces observations comparables entre elles.

Ce que couvre la normalisation
<img width="724" height="374" alt="Capture d&#39;écran 2026-09-06 065053" src="https://github.com/user-attachments/assets/7601b05d-69fb-429e-a7b9-9ec58618d111" />

9. Market Benchmark (Étape 7)
Principe

Le benchmark construit une référence de marché à partir des données normalisées. Exemple, après normalisation :

<img width="727" height="274" alt="Capture d&#39;écran 2026-09-06 065308" src="https://github.com/user-attachments/assets/bffa7289-9dd1-4fb9-a51a-fd6e7d334e67" />

On peut alors dire que le fournisseur du client est au-dessus du niveau de prix observé sur le marché. Mais le benchmark ne se limite pas à une moyenne.

Ce que le benchmark cherche à mesurer
Niveau central du marché — médiane, moyenne selon le cas
Dispersion — à quel point les prix sont éloignés les uns des autres
Position du fournisseur — où se situe son prix dans la distribution
Écart au benchmark — différence entre le fournisseur et la référence
Évolution du benchmark — comment le marché évolue dans le temps
Benchmark par segment, éventuellement — par origine, qualité, volume, destination, conditions commerciales, etc.

C'est précisément ici que la Normalisation (Étape 6) devient indispensable : on ne peut pas comparer des prix qui correspondent à des réalités commerciales différentes.

Ce que le benchmark ne dit PAS

Le Market Benchmark ne conclut jamais « le fournisseur est mauvais ». Il dit « voici comment son offre se positionne par rapport au marché observable ». Un fournisseur peut être 15 % plus cher que le benchmark tout en ayant une qualité supérieure ou des conditions commerciales qui justifient l'écart — c'est ensuite Supplier Analysis (Étape 8) qui croise ces éléments pour construire une analyse complète.

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

Le benchmark est recalculé à mesure que de nouvelles données arrivent, ce qui permet de suivre l'évolution du marché dans le temps et pas seulement une photo à un instant T. Exemple : benchmark actuel 7,20 €/kg vs benchmark précédent 6,95 €/kg → marché +3,6 %. Si le fournisseur du client passe en parallèle de 7,90 € à 8,10 €, le système peut constater que le fournisseur monte plus vite (ou moins vite) que le marché — une lecture beaucoup plus riche qu'un comparatif ponctuel isolé.

10. Supplier Analysis (Étape 8)
Séparation fondamentale des trois modules amont
<img width="726" height="204" alt="Capture d&#39;écran 2026-09-06 065805" src="https://github.com/user-attachments/assets/041890a6-ff78-4cf0-840a-37e4805ff096" />

Les 3 branches

Compétitivité (alimentée par l'interprétation du Market Benchmark, pas recalculée) :

Niveau de prix par rapport au marché
Évolution de son positionnement
Compétitivité selon les volumes/conditions
Écarts avec les alternatives

Performance (→ Supplier Performance Score /100) :

Stabilité des prix
Régularité des conditions
Évolution historique
Comportement par rapport au marché

Risque (→ Risk/Exposure Score /100) :

Dépendance
Volatilité
Anomalies
Concentration
Exposition à certaines conditions ou situations
Fiabilité — couche transversale, pas une 4ᵉ branche

Le Data Reliability construit à l'Étape 5 est réutilisé ici pour indiquer à quel point les conclusions sur ce fournisseur sont solides — conformément à ce qu'on avait déjà tranché en section 3 (Architecture).


Exemple concret :
<img width="729" height="118" alt="Capture d&#39;écran 2026-09-06 065936" src="https://github.com/user-attachments/assets/8ca3cae5-416e-4876-ab89-7d51739ccd42" />

En ne regardant que le prix, B semble clairement meilleur. Mais le système sait que l'information concernant B est beaucoup moins robuste. Supplier Analysis peut donc présenter une conclusion nuancée : « B est moins cher selon les données disponibles, mais cette conclusion repose sur des données significativement moins fiables. » — la Fiabilité ne change pas le résultat du calcul de Compétitivité/Performance/Risque, elle qualifie le niveau de confiance qu'on peut accorder à ce résultat.


11. Opportunity Engine (Étape 9)
Ce que le système sait déjà à ce stade

Avant l'Opportunity Engine, le système sait déjà : comment se situe le fournisseur par rapport au marché, s'il est compétitif, comment il performe, quels sont ses risques, et à quel point les données utilisées sont fiables.

La question posée

« Où est-ce que le client peut créer de la valeur ou réduire son risque ? »

Chacune des catégories d'opportunité répond directement à un ou plusieurs des 6 risques posés en section 1 (Problème identifié) :

<img width="723" height="634" alt="Capture d&#39;écran 2026-09-06 070543" src="https://github.com/user-attachments/assets/dacfad4b-3b4a-4624-aee6-129e5ba8459a" />

Anticipation / estimation future

À partir de l'historique et de la dynamique du marché, des modèles statistiques permettent d'estimer des scénarios futurs. Exemple : prix actuel 7,30 €/kg, scénario central à 3 mois 6,80 €/kg, intervalle possible 6,30-7,40 €/kg. L'Opportunity Engine peut alors détecter une opportunité potentielle de timing (évolution anticipée favorable), débouchant sur plusieurs stratégies possibles :

Renégocier maintenant — si le marché est susceptible de repartir à la hausse
Attendre — si le marché semble continuer à baisser
Fixer un prix futur / contractualiser — si l'estimation montre une fenêtre intéressante pour sécuriser les conditions
Augmenter ou réduire les volumes — selon le contexte

Et transversalement : le timing ne répond pas à un risque unique — il vient qualifier le "quand" pour n'importe lequel des risques ci-dessus (ex. le risque de dépendance peut justifier une diversification, mais le timing dit si c'est le bon moment de le faire ou s'il vaut mieux attendre).

Opportunité de maintien est le seul cas qui ne répond pas à un risque précis — elle correspond à l'absence de risque significatif détecté, une conclusion en soi utile pour le client (confirmation plutôt qu'alerte).

Recommandation (Étape 10)
Principe : jamais une instruction binaire

Le système ne donne jamais « renégociez » ou « ne renégociez pas », mais une décision accompagnée de son niveau d'incertitude et de scénarios quantifiés.

Exemple : plutôt que "le prix va probablement baisser", le système produit : prix actuel 7,40 €/kg, prix médian estimé à 3 mois 6,95 €/kg, probabilité que le prix soit inférieur à 7,00 €/kg dans 3 mois : 68 %, probabilité qu'il dépasse 7,80 €/kg : 12 %. Le client peut alors raisonner en termes de risque / rendement / timing, plutôt que de suivre une instruction brute.

Les scénarios quantifiés s'appuient sur la Simulation de Monte Carlo et l'inférence bayésienne, dont le fonctionnement est détaillé dans la section Continuous Intelligence (section 5) — la Recommandation est le point de sortie qui exploite ces scénarios, elle ne recalcule rien de nouveau.

Positionnement assumé

Le produit ne promet pas « nous savons ce qui va arriver », mais « nous quantifions les scénarios possibles, leur probabilité, et leur évolution à mesure que de nouvelles données apparaissent ».

Récapitulatif du pipeline complet (clôture de l'axe technique)
<img width="726" height="283" alt="Capture d&#39;écran 2026-09-06 071145" src="https://github.com/user-attachments/assets/ab5d747b-e643-44d8-b40e-ea1c111da40c" />

13. Continuous Intelligence

Section de référence unique — toute autre mention du document y renvoie (notamment depuis Opportunity Engine et Recommandation).

Principe

Le client active une surveillance périodique (ex. mensuelle/trimestrielle). Le prestataire ou les sources externes alimentent la base, et le système recalcule : benchmark, Supplier Performance Score, évolution des prix, évolution de la compétitivité, opportunités, alternatives.

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

Deux outils statistiques mobilisés
Simulation de Monte Carlo : générer de nombreuses trajectoires/scénarios possibles à partir des distributions et incertitudes observées — scénario défavorable / central / favorable / distribution complète — plutôt que de prétendre connaître un prix futur unique.
Inférence bayésienne : chaque nouvelle information (prix, transaction, changement de tendance...) met à jour les croyances/probabilités du modèle. À mesure qu'arrivent de nouveaux prix fournisseur, nouvelles transactions, nouvelles données de marché, changements de tendance, nouvelles informations qualitatives — le modèle met à jour ses estimations en continu.
Positionnement assumé

Le système ne promet pas « nous savons ce qui va arriver », mais « nous quantifions les scénarios possibles, leur probabilité, et leur évolution à mesure que de nouvelles données apparaissent ».

Rattachement à l'axe commercial

Accessible dès le Palier I (voir section 2, Fonctionnement global) — pas une 5ᵉ étape technique ni un 4ᵉ palier séparé, mais une option transversale activable depuis n'importe quel niveau de données déjà choisi par le client.


14. Méthodologie envisagée
Validation des étapes du pipeline

Les Étapes sont définies suffisamment clairement pour qu'une fois une étape terminée, il ne soit pas nécessaire d'y revenir. Cela dit, chaque résultat produit à une étape est scruté en continu pour vérifier sa cohérence avec les recherches et résultats des autres étapes — la validation n'est donc pas un aller simple, elle inclut un contrôle croisé permanent entre étapes plutôt qu'une validation isolée étape par étape.

Choix du marché/produit pilote

Aucun marché ou produit précis n'est encore fixé — ce choix sera dicté par le premier grossiste ou entreprise qui accordera sa confiance au porteur du projet, pas par une préférence personnelle. Tous les exemples utilisés dans la documentation (beurre de cacao/Ghana, huile cosmétique, farine) sont purement illustratifs. Une priorité générale est cependant assumée : cibler en priorité les grossistes de matières premières dans l'import-export.

Construction des formules de scoring

Pas de démarche encore arrêtée pour le calcul détaillé des formules (pondérations de Qualité/Fraîcheur/Provenance/Couverture, formule d'agrégation du Data Reliability, etc.) — ce travail sera approfondi plus tard. Engagement de méthode déjà pris : tout sera construit avec des logiciels précis et des technologies limitant au maximum le risque d'erreur (détail à venir dans la section Stack technique).

Horizon de la V1 "vendable"

Aucune échéance connue ni estimable à ce stade du projet — question jugée prématurée, comparable à demander un chiffre d'affaires prévisionnel avant même d'avoir un client. Ce point reste ouvert et ne sera clarifié qu'au fil de l'expérience terrain.

Travail en solo : contrainte financière, pas un choix de méthode définitif

Faire tout seul (acquisition, tri, qualification, benchmark, analyse, recommandation) est une contrainte financière actuelle, pas une préférence de fonctionnement à long terme. L'ambition est de faire grossir le projet suffisamment pour recruter progressivement :

Une équipe marketing/commerciale en priorité — pour la recherche de clients et la présentation/closing du produit, identifiée comme la tâche la moins appréciée par le porteur du projet lui-même.
Puis, progressivement, une délégation de la partie technique — recruter des spécialistes plus compétents que le porteur du projet sur chaque étape du pipeline.

Vision de long terme assumée : construire un système capable, à terme, de fonctionner sans dépendre exclusivement du porteur du projet — l'objectif classique de tout entrepreneur étant que l'entreprise puisse tourner de façon autonome, avec des experts spécialisés à chaque étape.



15. Stack technique
Outils par Étape
<img width="728" height="663" alt="Capture d&#39;écran 2026-09-06 073842" src="https://github.com/user-attachments/assets/2b74d353-a07c-46be-a7bc-228dedaed574" />
<img width="729" height="237" alt="Capture d&#39;écran 2026-09-06 073910" src="https://github.com/user-attachments/assets/45a08973-41b4-444a-991f-cbc9bf0ca3fe" />

Stack générale

<img width="724" height="322" alt="Capture d&#39;écran 2026-09-06 073942" src="https://github.com/user-attachments/assets/36c56138-ae1d-4587-a535-8748d0b7f24a" />

16. Ce qui reste à valider sur le terrain (synthèse complète)
Comment chaque grossiste gère actuellement ce problème (aucune méthode connue à l'avance)
Pourquoi cette visibilité manque aujourd'hui (hypothèses non confirmées)
Existence réelle d'un pôle data / spécialiste Procurement chez les grossistes ciblés (parfois le grossiste lui-même)
Nature exacte de la donnée additionnelle apportée à chaque Palier (au-delà de la logique générale D→E→F)
Faisabilité réelle du délai de livraison de moins d'un mois
Choix des 3-4 métriques les plus pertinentes pour la démo (Étape 0), variable par produit
Format définitif du rapport client (docx seul ou avec volet Excel)
Sources spécialisées (Catégorie E) et contacts de sous-traitance (Catégorie F), à identifier produit par produit
Recalcul du Data Reliability à chaque Palier (complet, choix par défaut) — à confirmer empiriquement face à un recalcul incrémental
Marché/produit du premier pilote (dépend entièrement du premier client)
Méthode précise de calcul des formules de scoring (pondérations, agrégation)
Échéance réaliste d'une V1 "vendable"
                    
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
        


Quelle profondeur historique doit-on fournir au client ?


12 mois glissants comme référence standard.

pour : 
saisonnalité ;
évolution des prix ;
différentes conditions de marché ;
plusieurs commandes ;
évolution du fournisseur ;
périodes de hausse/baisse ;
suffisamment d'observations pour commencer à comparer.

Mais ce n'est pas une règle absolue.

Si le fournisseur travaille avec le client depuis 3 ans, on peut exploiter davantage d'historique si cela apporte réellement quelque chose.

Et si la relation n'existe que depuis 5 mois, on travaille avec les 5 mois disponibles et on indique clairement la profondeur.

Donc :

12 mois = fenêtre standard de référence, pas obligation de disposer de 12 mois.


Le véritable produit est :

Donner au grossiste une vision actualisée de la compétitivité de ses achats par rapport au marché observable.

L'historique sert juste à :

comprendre + comparer + détecter + démontrer la valeur.


étudier des méthodologies existantes de price assessment / price discovery sur des marchés comparables, notamment commodities/OTC, comprendre comment elles traitent :

données asynchrones ;
transactions ;
bids/offers ;
différentes qualités ;
différents lieux ;
différents volumes ;
sources de fiabilité différente ;
manque de liquidité ;
observations aberrantes ;

puis déterminer ce qui est transposable à notre cas.


