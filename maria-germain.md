# Revue de code du TP1 de Maria Germain (par Théo Hautois)

## App.vue
1. le fichier App.vue a beaucoup de responsabilité, Il est préférable de confier la lecture/pause de la musique au composant *SongPlayer.vue*.

2.
````ts
function formatTime(timeValue : number) : string {
    const MIN = Math.floor(timeValue / 60);
    const SEC = Math.floor((timeValue - (MIN * 60)));
    return `${MIN < 10 ? '0' : ''}${MIN}:${SEC < 10 ? '0' : ''}${SEC}`;
}
````
Je pense que c'est mieux de faire le formatage du temps dans le composant *SongPlayerTime.vue*, puisque c'est lui qui s'occupe de l'affichage du temps.



## SongPlayer.vue
````ts
const props = defineProps<{
    selectedSongTitle: string;
    selectedSongArtistName : string;
    currentTime : string;
    duration : string;
    songIsPlaying: boolean;
}>()
````
L'utilisation d'un objet Song contenant toutes les informations d'une musique peut alléger le nombre de props du composant.


