# Checklist Audit FINMA

Checklist interactive pour l'audit financier des banques privées et gestionnaires de fortune suisses (OEPC-FINMA, Circ. FINMA 2020/1, NA-CH).

## Fonctionnalités

- **Suivi du mandat** : étapes Interim / Final / Completion avec sections Atlas, statut, responsables J/S/M, commentaires, jalons de sign-off et liens vers les checklists FSA
- **Documents PBC** : documents à demander au client pour chaque étape (Interim, Final, Completion, chaque FSA), statut à demander / demandé / reçu, recherche et copie de la demande client
- **Checklist par FSA** : objectif, priorités, documents à demander (PBC), signaux d'alerte, procédures détaillées (comment faire, piège fréquent, quoi faire en cas d'anomalie)
- **Statut par procédure** : À faire / Fait / Anomalie / N/A, avec avancement par FSA
- **Journal des anomalies** : description, montant et total, copiable vers Excel
- **Matrice des assertions**, **ICS / SCI** (NA-CH 890, contrôles clés par cycle) et **références réglementaires**
- Bascule **Banque privée / Gestionnaire de fortune**
- Thème clair / sombre automatique, utilisable sur mobile

## Utilisation

Ouvrir `index.html` dans un navigateur. Aucune installation, aucun serveur.

Pour une version en ligne : *Settings → Pages → Deploy from a branch → `main` / root*.

## Données

Les statuts, notes et anomalies sont enregistrés uniquement dans le navigateur (`localStorage`). Rien n'est envoyé sur un serveur. Ne saisis pas de données clients identifiantes.

## Modifier le contenu

Tout le contenu est dans le `<script>` de `index.html` :

- `PBC_RAW` : documents à demander par étape (les documents par FSA viennent de `FSA[].pbc`)
- `FSA` : une entrée par ligne d'état financier (`p` = procédures, `flags` = signaux d'alerte, `ics` = contrôles)
- `SCI` : démarche et contrôles par cycle
- `REF` : références réglementaires

## Avertissement

Base de travail générique. Ne remplace pas la méthodologie du cabinet ni le programme d'audit prudentiel FINMA. Vérifier la version en vigueur des textes cités.
