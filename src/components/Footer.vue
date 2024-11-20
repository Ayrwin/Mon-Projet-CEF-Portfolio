<script setup>
import { computed } from 'vue';
const copyright = computed(() =>{
    const currentYear = new Date().getFullYear()
    return 'Copyright ${currentYear} | Ayrwin Huet'
});
</script>

<template>
    <footer class="footer">
        <div class="footer__content">
            <div class="footer__adress">
                <h3>Mes Contacts</h3>
                <address>
                    <a href="mailto:ayrwin.huet@yahoo.fr">ayrwin.huet@yahoo.fr</a>
                    <a href="tel:0787233658">07.87.23.36.58</a>
                    <p>Poissy 78300</p>
                </address>
            </div>
            <div class="footer__borderRight"></div>
            <div class="footer__social">
                <h3>Me Retrouver</h3>
                <a class="footer__social__icon" href="https://github.com/Ayrwin">
                    <img src="../assets/img/github.jpg" alt="Logo Github">
                </a>
                <a class="footer__social__icon" href="https://www.linkedin.com/in/ayrwin-huet-4261109150">
                    <img src="../assets/img/linkedin.jpg" alt="Logo Linkedin">
                </a>
                <a class="footer__social__icon" href="https://www.facebook.com/ayrwin.huet">
                    <img src="../assets/img/Facebook.png" alt="Logo FaceBook">
                </a>
            </div>
        </div>
        <div class="footer__copyright">
            <p>Dernières modifications le<time datetime="2024-09-11">11 septembre 2024</time></p>
            <p class="copyright">{{ copyright }}</p>
        </div>
    </footer>
</template>

<style scoped>
.footer__content {
    display: flex;
    justify-content: space-evenly;
}

footer * {
    background-color: brown;
    color: antiquewhite;
    padding: 10px;
}

#footer {
    margin: 4em;
}

.footer__borderRight {
    border-right: 1px solid snow;
}

address {
    display: flex;
    flex-direction: column;
}

.footer__copyright {
    text-align: center;
}

time {
    font-style: italic;
}

.copyright {
    font-style: italic;
    font-size: 0.8em;
}

.footer__social__icon:hover {
    opacity: 50%;
}

img {
    height: 50px;
}
</style>