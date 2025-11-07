## Comment changer les projets affichés

Dans le fichier `assets/projects.json` se trouve tous les projets ainsi que leur description/images. Le format est le suivant (exemple de 2 projets):

```json
"Chien de pluie": {
   "description": "Description for Chien de pluie.",
   "images": [
   "./assets/placeholder.jpg",
   "./assets/placeholder2.jpg",
   "./assets/placeholder.jpg",
   "./assets/placeholder2.jpg",
   "./assets/placeholder.jpg"
   ]
},
"Landes de gascognes": {
   "description": "Description for Landes de gascognes.",
   "images": [
   "./assets/placeholder2.jpg",
   "./assets/placeholder.jpg",
   "./assets/placeholder2.jpg",
   "./assets/placeholder.jpg",
   "./assets/placeholder2.jpg"
   ]
},
```

- La première chaîne charactère correspond au nom du projet
- "description" correspond à la description du projet
- "images" correspond à toutes les images qui seront affichées dans le carrousel
  - à noter que pour les images, cela doit décrire le **chemin** vers l'image, **relatif** au fichier `index.html`. En l'occurence, il est recommandé de mettre tous les fichiers d'images dans le dossier `assets/` avec un nom contenant uniquement des lettres, chiffres ou tirets (`-` ou `_`).

<br>

## Comment ajouter un nouveau projet

2 étapes :

- mettre à jour `assets/projects.json` en ajoutant un nouveau projet (le plus simple est d'en duppliquer un existant et de changer le nom, description et images par ceux voulues)
- mettre à jour la section suivante dans le fichier `index.html` :

```html
<!-- list des projets -->
<div class="all-words">
  <span class="word">Chien de pluie</span
  ><span class="word">Landes de gascognes</span><span class="word">Éclairs</span
  ><span class="word">Reportages</span><span class="word">Notes</span
  ><span class="word">Confession d'un enfoiré</span>
</div>
```

Par exemple si on veut ajouter le projet "Nouveau Projet", le code devient alors :

```html
<!-- list des projets -->
<div class="all-words">
  <span class="word">Chien de pluie</span
  ><span class="word">Landes de gascognes</span><span class="word">Éclairs</span
  ><span class="word">Reportages</span><span class="word">Notes</span
  ><span class="word">Confession d'un enfoiré</span
  ><span class="word">Nouveau Projet</span>
</div>
```
