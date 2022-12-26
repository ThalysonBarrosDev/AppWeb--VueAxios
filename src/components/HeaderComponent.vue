<template>
    <header>
        <nav class="container">
            <a href="/"><img class="soon" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg" /></a>

            <img class="menu-button" v-on:click="openMenu" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg" />

            <div class="menu-overlay" v-if="menuActive" v-on:click="closeMenu"></div>

            <div class="menu-item" :class="{active:menuActive}">
                <img class="menu-soon" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg" />

                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/">Videos</a></li>
                    <li><a href="/">Sobre</a></li>
                    <li><a href="/">Contato</a></li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            menuActive: false
        }
    },
    methods: {
        openMenu: function() {
            this.menuActive = true;
        },
        closeMenu: function() {
            this.menuActive = false;
        }
    }
}
</script>

<style scoped>
header {
    background-color: var(--color-background-nav);
    height: 60px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

nav {
    display: flex;
    justify-content: space-between;
    height: 60px;
    align-items: center;
}

.soon {
    width: 130px;
}

.menu-button {
    width: 30px;
    cursor: pointer;
}

.menu-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 40%;
    height: 100vh;
    background-color: #000000;
    opacity: 0.8;
    cursor: pointer;
}

.menu-item {
    position: fixed;
    top: 0;
    right: 0;
    background-color: var(--color-background-nav);
    width: 60%;
    height: 100vh;
    display: none;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
}

.menu-soon {
    width: 110px;
    margin-top: 30px;
    margin-bottom: 10px;
}

.menu-item ul {
    list-style: none;
    text-align: center;
}

.menu-item ul li {
    margin: 20px 0;
}

.menu-item ul li a {
    color: var(--color-text-light);
}

.active {
    display: flex;
}

@media (min-width: 700px) {
    .menu-button, .menu-soon, .menu-overlay {
        display: none;
    }

    .menu-item {
        display: flex;
        position: static;
        height: 60px;
        width: auto;
    }

    .menu-item ul {
        display: flex;
        height: 60px;
        align-items: center;
    }

    .menu-item ul li {
        margin: 0;
        margin-left: 25px;
    }
}
</style>