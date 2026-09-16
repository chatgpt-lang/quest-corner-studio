# CLAUDE.md

## Projet
Quest Corner Visual Studio — éditeur HTML de visuels pour les lives de cartes Pokémon (déclinaison de F2K Visual Studio, identité Quest Corner). Voir [HANDOFF.md](HANDOFF.md) pour le contexte complet (accès, backend, secrets) et [README-QUEST-CORNER.md](README-QUEST-CORNER.md) pour les différences avec F2K.

## Autorisation de mise à jour autonome
Sarah (propriétaire du dépôt) a autorisé Claude à committer et pousser directement sur `main` sans demander confirmation à chaque fois, pour ce dépôt uniquement (choix fait le 2026-09-16). Les opérations destructives (force-push, reset --hard, réécriture d'historique, suppression de branches) restent soumises à confirmation explicite.

## Secrets
Ne jamais committer de clé API, webhook ou secret en clair (voir HANDOFF.md section 2). Les secrets vivent dans Make, Google Secret Manager ou les variables Cloud Run.
