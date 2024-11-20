<script setup>
import { ref } from 'vue'
let showMenu = ref( false )
</script>

<template>
    <header>
        <nav>
            <router-link class="link__img" to="/">
                <img src="../assets/img/logo-sekai.png" alt="Logo Sekai Fushigi">
            </router-link>
            <div class="sideNav__background" v-if="showMenu" @click="showMenu=false"></div>
            <div class="sideNav" v-if="showMenu">
                <span class="material-symbols-outlined link" @click="showMenu=false">close</span>
                <ul class="sideNav__list">
                    <RouterLink to="/#about" @click="showMenu=false">Présentation</RouterLink>
                    <RouterLink to="/#projet" @click="showMenu=false">Projet</RouterLink>
                </ul>
            </div>

            <div class="nav__link">
                <RouterLink id="about__link" to="/#about">Présentation</RouterLink>
                <span>|</span>
                <RouterLink id="project__link" to="/#projet">Projet</RouterLink>
            </div>
        </nav>
    </header>
</template>

<style scoped>
header {
    position: fixed;
    background-color: midnightblue;
    width: 83%;
    top: 0;
    padding: 5px;
    border-bottom: 1 px solid burlywood;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.link__img {
    padding: 5px;
}

img {
    display: flex;
    justify-content: center;
    width: 100px;
}

.nav__link * {
    font-size: 1.1em;
    padding: 5px;
    text-decoration: none;
}

.nav__link a {
    padding: 15px;
}

a:hover {
    background-color: coral;
    border-radius: 10px;
    text-decoration: underline;
}

.sideNav {
    width: 65%;
    height: 100%;
    box-sizing: border-box;
    position: fixed;
    top: 85px;
    right: 0;
    background-color: aliceblue;
    padding: 10px;
    border: 1px solid #060640;
    border-top: none;
    border-right: none;
}

.sideNav__background {
    position: fixed;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
}

.sideNav__list {
    display: flex;
    flex-direction: column;
    gap: 15px;
    font-size: 1.1em;
    padding-right: 1em;
}

.link {
    cursor: pointer;
}

.nav__link {
    display: flex;
}

</style>