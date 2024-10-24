<script setup>
import TitreNiveau2 from './TitreNiveau2.vue';

const parcours = {
    annee1: {
        ecole: 'Lycée Charles de Gaulles',
        date: 'Juil 2015',
        title: 'Bac STI2D',
        comment: 'Baccalauréat technologique Sciences et Technologies Industrie et du Développement Durable'
    },

    annee2: {
        ecole: 'Lycée Léonard de Vinci',
        date: 'Juil 2017',
        title: 'BTS Electrotechnique',
        comment: 'Diplôme Etudes Supérieures en Electrotechnique'
    },

    annee3: {
        ecole: 'La Mission Locale de Poissy',
        date: 'Oct 2017 - Mars 2018',
        title: 'Parcours Intensif de Formation et Accès à Emploi',
        comment: 'Aide à la Recherche Emploi'
    },
}
</script>

<template>
    <div class="courses">
        <div class="courses__title">
            <span class="material-symbols-outlined">écoles</span><br>
            <TitreNiveau2>Mon parcours</TitreNiveau2>
        </div>

        <div class="parcours">
            <div class="ecole" v-for="annee in parcours">
                <h3 class="ecole__title">{{ annee.ecole }}</h3>
                <h4 class="ecole__info">{{ annee.title }} <span class="separation">|</span> {{ annee.date }}</h4>
                <p class="ecole__comment">{{ annee.comment }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.courses {
    width: 60%;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: auto;
}

.courses__title {
    text-align: center;
}

.material-symbols-outlined {
    font-size: 4em;
}

.ecole__title {
    font-size: 1.25em;
}

.ecole__info {
    font-size: 1.05em;
}

.separation {
    font-style: italic;
    color: #A0006D;
}

.ecole__comment {
    text-indent: 2em;
    text-align: justify;
}

.parcours {
    margin-top: 15px;
    display: flex;
    flex-direction: column-reverse;
    gap: 25px;
}

.ecole {
    padding: 15px;
    background-color: yellowgreen;
    border-radius: 25px;
    box-shadow: -4px 5px 10px #060640;
}

</style>