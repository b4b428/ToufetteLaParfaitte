# Toufette la parfaite

Planning des repas de la semaine (midi, goûter, soir), bibliothèque de recettes, liste de courses calculée toute seule, et impression. Toufette, l'assistante de l'outil, propose des menus, estime les calories, importe des recettes depuis un lien et adapte une recette au Cookeo ou à un objectif de calories.

Tout tient dans un seul fichier, `index.html`. Pas de serveur, pas de base de données, pas d'installation.

## Ce que ça fait

- **Planning** : 7 jours × 3 repas, nombre de personnes réglable case par case, calories estimées par personne, fiche recette ouvrable d'un clic (📄), lien direct vers la recette, navigation d'une semaine à l'autre.
- **Propositions** : un plat pour une case, ou toute la semaine d'un coup. Même plat lundi et mardi, et jeudi et vendredi (à cuisiner une fois pour deux jours), rien le dimanche soir, et jamais un plat déjà proposé ou servi les semaines voisines.
- **Chercher des idées** : depuis une case, des mots-clés (ingrédients à écouler, envies, « rapide ») donnent 4 propositions de plats, classiques ou originaux, à choisir d'un clic.
- **Adapter une recette** : depuis une case, version Cookeo (modes, durées, liquides revus) et/ou objectif de calories par personne, avec les quantités réajustées. La recette d'origine est conservée.
- **Recettes** : import depuis un lien, depuis un texte collé, ou saisie à la main. Un favori « Copier pour Toufette » dépanne sur les sites difficiles à lire.
- **Liste de courses** : quantités ajustées au nombre de personnes, ingrédients identiques additionnés (500 g + 1 kg = 1,5 kg), rangés par rayon, avec articles à cocher et ajouts libres.
- **Impression** : planning en A4 paysage, liste de courses en A4 portrait, et fiche recette d'un repas (ou de toute la semaine) avec les quantités du jour.

## Mise en ligne sur GitHub Pages

1. Déposez `index.html` à la racine du dépôt (bouton **Add file → Upload files**, puis **Commit changes**).
2. Onglet **Settings → Pages**. Sous *Build and deployment*, choisissez la source **Deploy from a branch**, la branche **main** et le dossier **/ (root)**, puis **Save**.
3. Après une minute ou deux, la page est en ligne à l'adresse indiquée en haut de cet écran.

Sur téléphone, « Ajouter à l'écran d'accueil » depuis le navigateur donne une icône comme une application.

## Première utilisation

Sans clé d'API, tout fonctionne sauf Toufette : planning, recettes saisies à la main, liste de courses, impression.

Pour activer Toufette, chaque personne met **sa propre** clé, dans « Réglages et sauvegarde » :

1. Créez un compte sur [console.anthropic.com](https://console.anthropic.com) (c'est un compte développeur, distinct d'un abonnement Claude).
2. Ajoutez un crédit prépayé dans *Billing*, et un plafond mensuel dans *Limits* pour être tranquille.
3. *API Keys* → *Create Key*, copiez la clé (elle commence par `sk-ant-` et ne s'affiche qu'une seule fois, à sa création).
4. Dans l'outil : « Réglages et sauvegarde », collez la clé, puis « Tester la clé ».

La clé est gardée dans le navigateur de la personne. Elle n'est jamais écrite dans ce dépôt, ni dans les sauvegardes, et n'est envoyée qu'à Anthropic. Vous pouvez donc partager l'adresse : chacun paie son propre usage, et personne ne voit les menus des autres.

## Données

Menus, recettes et listes sont enregistrés dans le navigateur de chaque personne (`localStorage`). Il n'y a pas de synchronisation automatique entre appareils : « Réglages et sauvegarde » permet de télécharger un fichier de sauvegarde et de le restaurer ailleurs.

## Modifier l'outil

Tout est dans `index.html` : HTML, CSS et JavaScript, sans dépendance. Seules les polices viennent de Google Fonts, et le logo est intégré dans le fichier. Le modèle utilisé par Toufette se change dans les réglages.

## Crédits

Logo « Toufette la parfaite » fourni par l'auteur du dépôt. Outil construit avec Claude (Anthropic).
test pour deploiement
