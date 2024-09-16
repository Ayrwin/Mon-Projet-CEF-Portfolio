<script setup>
import TitreNiveau2 from './TitreNiveau2.vue';

const parcours = {
    annee1: {
        entreprise: 'Groupe ACTUAL INtérim',
        date: 'Oct 2017 - Mars 2018',
        title: 'Electricien de Chantier',
        comment: 'Missions : Tirage de câble ; Installation système incendie ; Lire des plans et les suivre correctement'
    },

    annee2: {
        entreprise: 'OK Services',
        date: 'Mai 2019 - Juil 2019',
        title: 'Technicien itinérant',
        comment: 'Missions : Installation de système de sécurité chez des particuliers ; Dépannage ou Réparation pour tous autres problèmes'
    },
}
</script>

<template>
    <div class="experience">
        <div class="experience__title">
            <span class="material-symbols-outlined">work</span><br>
            <TitreNiveau2>Mes expériences professionnelles</TitreNiveau2>
        </div>

        <div class="annee">
            <div class="job" v-for="annee in parcours">
                <h3 class="job__title">{{ annee.entreprise }}</h3>
                <h4 class="job__info">{{ annee.title }} <span class="separation">|</span>{{ annee.date }}</h4>
                <p class="job__comment">{{ annee.comment }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.experience {
    width: 60%;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: auto;
}

.experience__title {
    text-align: center;
}

.material-symbols-outlined {
    font-size: 4em;
}

.job__title {
    font-size: 1.25em;
}

.job__info {
    font-size: 1.05em;
}

.separation {
    font-style: italic;
    color: blueviolet;
}

.job__comment {
    text-indent: 2em;
    text-align: justify;
}

.annee {
    margin-top: 15px;
    display: flex;
    flex-direction: column-reverse;
    gap: 25px;
}

.job {
    padding: 15px;
    background-color: brown;
    border-radius: 25px;
    box-shadow: -4px 5px 1px #0606;
}

</style>