# 5. Architecture de Référence FLOW

## En quelques mots

Cette section décrit l'architecture de référence du programme FLOW.

Elle présente les capacités technologiques partagées, les capacités métier partagées, le modèle métier de référence, les domaines métier et les principales vues d'architecture.

## Positionnement

FLOW se positionne entre les canaux de vente, les systèmes cœur et les acteurs d'exécution. Il ne remplace pas l'ERP : il porte la logique d'engagement, d'orchestration, de décision et de suivi transverse.

> ERP horizontal transactionnel + FLOW vertical d'engagement et d'orchestration.

## Vue d'ensemble logique

FLOW doit permettre de capter une demande, qualifier son contexte, décider de la meilleure promesse, orchestrer son exécution et mesurer son résultat.

Les blocs logiques de référence sont :

- **Experience APIs** : interfaces exposées aux canaux, frontaux et partenaires.
- **Case Management** : cycle de vie de la demande, décisions, exceptions, statuts métier.
- **Rules & Decisioning** : règles de promesse, allocation, priorisation, éligibilité, substitution.
- **Inventory Visibility** : stock consolidé, stock réservé, stock promis, stock projeté.
- **Event Bus** : publication des événements métier et intégration asynchrone.
- **MDM / référentiels** : produit, client, point de stockage, organisation, contrat.
- **Data Hub** : observabilité métier, performance, apprentissage, pilotage.

## Business capabilities couvertes

### Engagement client & contrat

Capturer la demande, identifier le client, appliquer les conditions commerciales, gérer les assortiments, prix, remises, contraintes B2B/B2C et engagements contractuels.

Capacités associées :

- customer & account context ;
- sales conditions ;
- assortment eligibility ;
- order capture ;
- case lifecycle.

### Promesse & stock

Calculer ce qui peut être promis, à quelle date, depuis quel point de stockage, avec quelle priorité et quel risque.

Capacités associées :

- inventory visibility ;
- ATP / Available to Promise ;
- reservation ;
- allocation ;
- substitution & split.

### Orchestration fulfilment

Transformer la promesse en exécution : sourcing, préparation, expédition, annulation, retour, exception, reprise ou compensation.

Capacités associées :

- sourcing decision ;
- warehouse / store fulfilment ;
- transport routing ;
- return orchestration ;
- exception handling.

### Finance & pilotage

Produire les événements de gestion nécessaires aux écritures, au contrôle, au rapprochement et au pilotage de la performance.

Capacités associées :

- Compte Rendu d'Événement ;
- déclencheurs de reconnaissance de revenu ;
- allocation de coûts ;
- KPIs opérationnels ;
- audit trail.

## Patterns d'intégration

- API synchrone pour la promesse et les décisions nécessitant une réponse immédiate.
- Événements métier pour propager les changements d'état significatifs.
- CRE pour la traduction finance/gestion des événements opérationnels.
- Anti-corruption layer entre FLOW et les ERP/WMS/OMS existants.
- Observabilité transverse : corrélation case, commande, stock, expédition, finance.

## Candidats techniques

Les candidats techniques restent à arbitrer selon les standards groupe, mais la cible peut s'appuyer sur :

- Spring Boot ou Quarkus pour les services métier ;
- Kafka pour l'événementiel ;
- Drools / DMN pour certaines règles de décision ;
- Temporal si un besoin d'orchestration technique durable apparaît ;
- API Gateway, OpenAPI et AsyncAPI pour les contrats d'intégration ;
- un data lakehouse pour l'observabilité, le pilotage et l'apprentissage.

## Sections prévues

- 5.1 Vue d'ensemble
- 5.2 Capacités Technologiques Partagées
- 5.3 Capacités Métier Partagées
- 5.4 Modèle Métier de Référence
- 5.5 Domaines Métier
- 5.6 Architecture Applicative
- 5.7 Architecture Data
- 5.8 Architecture d'Intégration
- 5.9 Architecture de Sécurité
