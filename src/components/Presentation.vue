<script setup>
import { ref } from 'vue';
</script>

<template>
  <div id="about">
    <div class="presentation">
      <div class="presentation__text">
        <TitreNiveau2>Présentation</TitreNiveau2>
        <p>Bonjour à vous, je suis Ayrwin Huet. Je suis un développeur web débutant qui veut s'améliorer en front-end et back-end. <br>
          Dans ce portfolio découvrez mon projet. <br>
          Hâte de discuter avec vous et pouvoir vous aidez dans vos projets.
        </p>
        <RouterLink class="CTA" :to="{hash:'#contact'}">Me Contacter</RouterLink>
      </div>

      <img src="../assets/img/Photo Ayrwin.jpg" alt="Photo d'Ayrwin">
    </div>

    <div class="about__filter">
      <button class="about__filter__button CTA" @click="presentationFilter='CV'">CV</button>
    </div>
    <div class="about__content">
      <CV v-if="presentationFilter === 'CV'"/>
      <a class="CV" href="https://github.com/Ayrwin/Mon-CV.git"></a>
    </div>
  </div>
</template>

<style scoped>
.presentation {
  background-color: blueviolet;
  display: flex;
  padding: 10px 10%;
  gap: 20px;
  align-items: center;
}

.presentation__text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 15px;
}

.presentation__text p {
  width: 60%;
  text-align: justify;
  text-indent: 5%;
}

img {
  width: 25%;
  height: 25%;
  border-radius: 50%;
  box-shadow: -4px 5px 25px palevioletred;
}

.about__filter {
  display: flex;
  gap: 15px;
  margin: 15px 0;
  justify-content: center;
}

.about__content {
  margin-bottom: 15px;
  margin-bottom: 2em;
}

</style>