<template>
    <footer>
        <a class="social-link" target="_blank" v-for="(socialLink, index) in socialLinks" :key="index" :href="socialLink.link">
            <img :src="socialLink.icon" />
        </a>
    </footer>
</template>

<script>
import api from '@/services/api.js';

export default {
    name: 'FooterComponent',
    data() {
        return {
            socialLinks: []
        }
    },
    mounted() {
        api.get('/social-links.json').then(response => {
            this.socialLinks = response.data;
        });
    }
}
</script>

<style scoped>
footer {
    widows: 100%;
    height: 60px;
    background-color: var(--color-background-nav);
    display: flex;
    justify-content: center;
    align-items: center;
}

.social-link {
    border: 2px solid var(--color-text-light);
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    margin: 0 10px;
}

.social-link img {
    width: 20px;
}
</style>