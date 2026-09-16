# CLAUDE.md

## Projet
Quest Corner Visual Studio — éditeur HTML de visuels pour les lives de cartes Pokémon (déclinaison de F2K Visual Studio, identité Quest Corner). Voir [HANDOFF.md](HANDOFF.md) pour le contexte complet (accès, backend, secrets) et [README-QUEST-CORNER.md](README-QUEST-CORNER.md) pour les différences avec F2K.

## Ce dossier est la copie canonique
Ce dossier (`Documents/Codex/2026-08-14/.../outputs/quest-corner-studio`) est la vraie copie de travail — assets et backend `render-service/` inclus. Le dépôt GitHub `chatgpt-lang/quest-corner-studio` avait divergé (une version "démo" allégée, sans assets ni backend, poussée séparément) ; réconcilié le 2026-09-16 pour que `main` corresponde à ce dossier. Un second clone existe dans `~/code/quest-corner-studio` mais ne doit plus être utilisé pour ce projet.

## Autorisation de mise à jour autonome
Sarah (propriétaire du dépôt) a autorisé Claude à committer et pousser directement sur `main` sans demander confirmation à chaque fois, pour ce dépôt uniquement (choix fait le 2026-09-16). Les opérations destructives (force-push, reset --hard, réécriture d'historique, suppression de branches) restent soumises à confirmation explicite.

## Emplacements d'éléments figés
Le fichier `index.html` contient une grande table `states={...}` (clés `'live::format[::count]'`) qui semble être une ancienne tentative de mise en page validée, mais elle n'est jamais lue par `key()`/`load()` (qui utilisent le préfixe `'live-quest-v2::'`) — probablement orpheline/obsolète, à ne pas prendre pour référence. Les emplacements réellement actifs sont ajoutés juste après cette table, sous forme d'entrées `states['live-quest-v2::<format>::<count>']=...`, avec un commentaire horodaté au-dessus de chaque ajout.

## Secrets
Ne jamais committer de clé API, webhook ou secret en clair (voir HANDOFF.md section 2). Les secrets vivent dans Make, Google Secret Manager ou les variables Cloud Run.
