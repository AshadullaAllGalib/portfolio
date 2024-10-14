<script setup>
import { RouterLink, useRoute } from 'vue-router';
import { ref } from 'vue';
const isMenuOpen = ref(false);
const isActiveLink = (routePath) => {
    const route = useRoute();
    return route.path === routePath;
}
</script>

<template>
    <header>
        <nav class="navbar">
            <RouterLink to="/" class="nav-logo">
                <img src="../assets/images/logo.png" alt="Logo" />
            </RouterLink>

            <ul class="nav-menu" :class="{ 'active': isMenuOpen }"
                @click.prevent="isMenuOpen = !isMenuOpen">
                <li class="nav-item">
                    <RouterLink to="/"
                        :class="[isActiveLink('/') ? 'nav-link-active' : 'nav-link']">
                        Home</RouterLink>
                </li>
                <li class="nav-item">
                    <RouterLink to="/about"
                        :class="[isActiveLink('/about') ? 'nav-link-active' : 'nav-link']">About
                    </RouterLink>
                </li>
                <li class="nav-item">
                    <RouterLink to="/experience"
                        :class="[isActiveLink('/experience') ? 'nav-link-active' : 'nav-link']">
                        Experience
                    </RouterLink>
                </li>
                <li class="nav-item">
                    <RouterLink to="/contacts"
                        :class="[isActiveLink('/contacts') ? 'nav-link-active' : 'nav-link']">
                        Contacts
                    </RouterLink>
                </li>
            </ul>

            <div class="hamburger" :class="{ 'active': isMenuOpen }"
                @click.prevent="isMenuOpen = !isMenuOpen">
                <span class="bar"></span>
                <span class="bar"></span>
                <span class="bar"></span>
            </div>
        </nav>
    </header>
</template>

<style scoped>
header {
    background-color: rgb(40, 77, 128);
    position: fixed;
    width: 100%;
    z-index: 1000;
}

li {
    list-style: none;
}

a {
    text-decoration: none;
    color: #fff;
}

.navbar {
    min-height: 70px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 80%;
    margin: 0 auto;
}


.navbar .nav-logo {
    width: 50px;
    height: 50px;
}

.navbar .nav-logo img {
    width: 50px;
    height: 50px;
    border-radius: 100%;
}

.nav-menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav-item {
    display: flex;
    align-items: center;
}

.nav-link {
    transition: 0.7s ease;
    font-size: 18px;
    height: 70px;
    display: flex;
    align-items: center;
    padding: 0 30px;

}

.nav-link:hover {
    background: rgb(1, 51, 116);
}

.nav-link-active {
    background: rgb(1, 51, 116);
    font-size: 18px;
    height: 70px;
    display: flex;
    align-items: center;
    padding: 0 30px;
}

.hamburger {
    display: none;
    cursor: pointer;
}

.bar {
    display: block;
    width: 30px;
    height: 3px;
    margin: 5px auto;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
    background-color: #fff;
}

@media (max-width: 768px) {
    .navbar {
        width: auto;
        padding: 0 40px;
    }

    .hamburger {
        display: block;
    }

    .hamburger.active .bar:nth-child(2) {
        opacity: 0;
    }

    .hamburger.active .bar:nth-child(1) {
        transform: translateY(8px) rotate(45deg);
    }

    .hamburger.active .bar:nth-child(3) {
        transform: translateY(-8px) rotate(-45deg);
    }

    .nav-menu {
        position: fixed;
        top: 70px;
        bottom: 0;
        right: -100%;
        gap: 0;
        justify-content: flex-start;
        flex-direction: column;
        background-color: rgba(48, 86, 136, 0.87);
        width: 100%;
        text-align: center;
        transition: 0.3s;
    }

    .nav-item {
        margin: 10px;
        height: 40px;
    }

    .nav-link {
        font-size: 20px;
    }

    .nav-menu.active {
        right: 0;
    }
}
</style>