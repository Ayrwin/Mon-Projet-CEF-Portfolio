<script setup>
import TitreNiveau2 from './TitreNiveau2.vue';

const competences = ['HTML','CSS','JavaScript','Vue.JS']

const languages = [
    {
        name: "Français",
        level: "Langue maternelle"
    },
    {
        name: "Anglais",
        level: "Avancé"
    },
    {
        name: "Allemand",
        level: "Débutant"
    },
]

const tools = [
    {
        name: 'Systèmes',
        liste: 'Git, GitHub, Windows'
    },
    {
        name: 'Bureautique',
        liste: 'MicroSoft Office'
    },
]

const hobbies = [
    {
        name: 'Jeux Vidéos'
    },
    {
        name: 'Culture Japonaise'
    },
    {
        name: 'Sports',
        liste: ['Natation','Jujitsu','Escrime Médiéval']
    },
]
</script>

<template>
    <div class="competences">
        <div class="left__column">
            <div class="skills">
                <div class="skills__title">
                    <span class="material-symbols-outlined"></span><br>
                    <TitreNiveau2>Mes Compétences Techniques</TitreNiveau2>
                </div>
                <div class="skills__content">
                    <li v-for="i in competences" class="competences">{{ i }}</li>
                </div>
            </div>

            <div class="languages">
                <div class="languages__title">
                    <span class="material-symbols-outlined"></span>
                    <TitreNiveau2>Langues</TitreNiveau2>
                </div>
                <div class="languages__content">
                    <li v-for="i in languages" class="language">
                        {{ i.name }} : {{ i.level }}
                    </li>
                </div>
            </div>
        </div>

        <div class="right__column">
            <div class="outils">
                <div class="outils__title">
                    <span class="material-symbols-outlined"></span>
                    <TitreNiveau2>Outils maîtrisés</TitreNiveau2>
                </div>
                <div class="outils__content">
                    <ul>
                        <li v-for="i in tools" class="tool">
                            {{ i.name }} : {{ i.liste }}
                        </li>
                    </ul>
                </div>
            </div>

            <div class="hobbies">
                <div class="hobbies__title">
                    <span class="material-symbols-outlined"></span>
                    <TitreNiveau2>Centres d'Intérêt</TitreNiveau2>
                </div>
                <div class="hobbies__content">
                    <ul>
                        <li v-for="i in hobbies" class="hobby">
                            {{ i.name }}
                            <ul>
                                <li class="sousListe" v-for="e in i.liste">{{ e }}</li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.competences {
    width: 60%;
    display: flex;
    flex-direction: row;
    align-items: center;
    margin: auto;
    align-content: center;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
}

.skills, .languages, .outils, .hobbies {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: auto;
    margin-top: 15px;
}

.skills__title, .languages__title, .outils__title, .hobbies__title {
    display: flex;
    align-items: center;
    text-align: center;
}

.material-symbols-outlined {
    font-size: 2.5em;
}

.skills__content, .languages__content {
    margin-top: 15px;
    display: flex;
    gap: 15px;
    flex-wrap: wrap;
    justify-content: center;
}

.competence, .language {
    list-style: none;
    color: whitesmoke;
    background-color: orangered;
    padding: 5px 1em;
    border-radius: 1em;
    box-shadow: -4px 4px 10px darkmagenta;
}

.tool, .hobby {
    margin-top: 10px;
    text-align: start;
}

.sousListe {
    list-style-type: circle;
}

.hobbies__content, .outils__content {
    align-self: flex-start;
    margin: 15px 0;
}

</style>