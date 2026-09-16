# Quest Corner Visual Studio — démo

Cette démo est une duplication indépendante de F2K Visual Studio, adaptée à l’identité de Quest Corner.

## Identité appliquée

- Bleu principal : `#263D52`
- Doré principal : `#E8B747`
- Logo : `assets/brand/quest-corner-logo.png`
- Nom affiché : `Quest Corner Visual Studio`
- Fond par défaut : motif bleu et doré Quest Corner
- Variante : motif vert et doré (portrait et bannière large)

Le fond blanc et l’ancien fond extérieur ont été retirés de l’interface. La banque d’éléments est maintenant séparée en deux rubriques, « Pokémon » et « Objets graphiques ». Cette dernière contient le séparateur doré, l’étoile et le cartouche fournis.

L’atelier « Complète ta collection » devient « Nouveautés » et propose les formats Story, Bannière Web (1890 × 600 px) et Bannière Mobile (1260 × 400 px). « L’arbre du live » devient « Meilleur drop » : l’arbre est supprimé et 1 à 3 cartes sont centrées dans la composition. Les cartes décoratives animées en arrière-plan sont désactivées dans tous les ateliers.

L’atelier « Annonce de live » utilise désormais deux textes en partie haute, sans macaron de prix ni cadre autour du nom de série. Les produits sont abaissés et décalés vers la gauche, et l’ancien logo Voggt est remplacé par le logo eBay Live fourni.

## Fonctionnalités conservées

Les cinq ateliers, les formats Story/Post/Miniature/Bannières, les placements, animations, imports, bibliothèques, sélection multiple, annulation, couleurs, fonds, exports PNG/vidéo, détourage et Chat Sarah sont conservés.

Le stockage local du navigateur utilise des clés `quest-corner-*` séparées de celles de F2K. Les compositions et bibliothèques des deux studios ne se mélangent donc pas.

## Ouvrir localement

Depuis le dossier du projet :

```bash
python3 -m http.server 8767 --bind 127.0.0.1
```

Puis ouvrir `http://127.0.0.1:8767/`.

## Important avant publication

La copie contient le moteur de rendu de F2K pour faciliter une future intégration, mais elle n’est pas encore déployée sur une URL Quest Corner. Avant une mise en ligne client, créer un dépôt et un service propres, puis remplacer ou configurer les accès Make, PhotoRoom et Cloud Run.
