---
outline: deep
---

# Revue de code du TP01 de Théo Hautois

Cette page documente son app SongPlayer

## Le code

### Gestion des props:
Très bonne, l'utilisation d'un type Song permet de bien partager l'information entre les composants
```ts
    defineProps({
        currentMusic:{type:Song, required:false}
    })
```
### Gestion des emit
Très bonne
```ts
  const emit = defineEmits(['music-change','error-api'])
```

### Classe Song & Artist
Très complète, pas seulement un type Song. Classe avec des attibuts. Même chose pour Artist.

### Gestion des erreurs
Très bonne gestion des erreurs. Le style des messages ext vraiment très cool. Tous les cas sont couverts.

### Autre
Pas de non pour le lecteur (index.html)


