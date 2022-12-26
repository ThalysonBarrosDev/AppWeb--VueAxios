<template>
    <main>
        <div class="text-top">Vídeos novos toda <b>Quinta às 20:00</b></div>

        <a href="https://youtube.com/wdevoficial" target="_blank">
            <img class="subscribe" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg" />
        </a>

        <div class="text-bottom">Youtube.com/wdevoficial</div>
    </main>
</template>

<script>
export default {
    name: 'HomeView'
}
</script>

<style scoped>
main {
    background-color: var(--color-background-home);
    justify-content: center;
    align-items: center;
}

.text-top {
    color: var(--color-text-light);
    font-size: 22px;
    margin-bottom: 20px;
}

.subscribe {
    width: 300px;
}

.text-bottom {
    color: var(--color-text-light);
    font-size: 18px;
    margin-top: 20px;
}
</style>