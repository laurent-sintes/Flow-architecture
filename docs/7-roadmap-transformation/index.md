# 7. Roadmap de Transformation

## En quelques mots

Cette section décrit la trajectoire permettant de passer de l'existant à l'architecture de référence FLOW.

La trajectoire doit rester incrémentale : l'objectif n'est pas de remplacer d'un coup l'ensemble ERP / OMS / WMS / TMS, mais de construire progressivement un socle d'engagement, de décision, d'intégration et d'observabilité.

## 7.1 Principes de Transformation

- Avancer par **capability** plutôt que par application isolée.
- Choisir des cas d'usage qui révèlent les vrais problèmes de promesse, stock, fulfilment et finance.
- Ne pas masquer les exceptions : les utiliser pour apprendre et améliorer le modèle.
- Séparer les décisions métier des intégrations techniques.
- Sécuriser une trajectoire compatible avec l'existant et la cible ERP.

## 7.2 Vagues de Transformation

### Phase 0 — Cadrage

Objectif : stabiliser la vision et le vocabulaire.

Travaux clés :

- valider la vision FLOW ;
- cartographier les demandes métier prioritaires ;
- identifier les systèmes impliqués ;
- recenser les règles critiques de promesse, stock, allocation et fulfilment ;
- définir les premiers indicateurs de succès.

### Phase 1 — Socle d'architecture

Objectif : établir les fondations techniques et fonctionnelles.

Travaux clés :

- définir le modèle de case ;
- définir les événements métier et la corrélation ;
- construire les premières APIs d'engagement ;
- brancher un périmètre pilote sur stock, commande et fulfilment ;
- rendre les règles observables et gouvernables.

### Phase 2 — Pilote métier

Objectif : démontrer la valeur sur un périmètre limité mais représentatif.

Cas candidats :

- ship-from-store ;
- allocation B2B ;
- retour cross-canal ;
- promesse stock ;
- orchestration d'exception.

Mesures :

- délai de promesse ;
- taux d'exception ;
- qualité stock ;
- respect de la promesse ;
- effort opérationnel de résolution.

### Phase 3 — Extension

Objectif : étendre la couverture et rationaliser progressivement.

Travaux clés :

- étendre par capability ;
- rationaliser les OMS et orchestrateurs redondants ;
- industrialiser les patterns d'intégration ;
- renforcer le modèle de données partagé ;
- préparer l'alignement avec la trajectoire ERP cible.

## 7.3 Architectures de Transition

Chaque vague doit produire une architecture de transition explicite :

- périmètre fonctionnel couvert ;
- systèmes intégrés ;
- contrats d'API et d'événements ;
- règles embarquées ;
- données de référence utilisées ;
- dette assumée ;
- critères de passage à la vague suivante.
