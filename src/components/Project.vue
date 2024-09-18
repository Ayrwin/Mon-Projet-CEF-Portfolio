<script setup>
    import { ref } from 'vue'

    import TitreNiveau2 from '../components/TitreNiveau2.vue';
    import SmallCard from '../components/Project_SmallCard.vue';
    import Modal from '../components/Modal.vue';

    let showModal = ref( false ) 
    let msgToModal = ref('')
</script>

<template>
    <div id="projet">
        <div class="projet__title">
            <span class="material-symbols-outlined">terminal</span>
            <TitreNiveau2>Projet</TitreNiveau2>
        </div>

        <div class="smallCard__box">
            <SmallCard @click="showModal=true; msgToModal=i" v-for="i in project" :projet="i"></SmallCard>
        </div>
        <Modal v-if="showModal" @close="showModal = false" :projet="msgToModal"></Modal>
    </div>
</template>

<style scoped>
    button {
        border: none;
        background-color: wheat;
    }

    #projet {
        background-color: wheat;
        padding: 15px 0px;
    }

    .material-symbols-outlined {
        font-size: 2em;
    }

    .projet__title {
        display: flex;
        align-items: start;
        gap: 5px;
        justify-content: center;
    }

    .smallCard__box {
        margin: 20px auto;
        width: 60%;
        display: flex;
        gap: 25px;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
    }

    .SmallCard {
        flex-basis: 30%;
        max-width: 270px;
        min-width: 270px;
    }

</style>