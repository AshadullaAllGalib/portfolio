<script setup>
import { ref } from 'vue';

// const hamburger = ref(document.querySelector(".hamburger"));
// const navMenu = ref(document.querySelector(".nav-menu"));

// hamburger.addEventListener("click", () => {
//     hamburger.classList.toggle("active");
//     navMenu.classList.toggle("active");
// })

// document.querySelectorAll(".nav-link").forEach(n => n.addEventListener("click", () => {
//     hamburger.classList.remove("active");
//     navMenu.classList.remove("active");
// }))

</script>

<template>
    <header>
        <nav class="navbar">
            <a href="#" class="nav-logo">
                <img src="../assets/images/logo.PNG" alt="Logo" />
            </a>

            <ul class="nav-menu">
                <li class="nav-item">
                    <a href="#" class="nav-link">Home</a>
                </li>
                <li class="nav-item">
                    <a href="#" class="nav-link">About</a>
                </li>
                <li class="nav-item">
                    <a href="#" class="nav-link">Experience</a>
                </li>
                <li class="nav-item">
                    <a href="#" class="nav-link">Contacts</a>
                </li>
            </ul>

            <div class="hamburger">
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
    gap: 60px;
}

.nav-link {
    transition: 0.7s ease;
}

.nav-link:hover {
    color: rgb(2, 40, 78);
}

.hamburger {
    display: none;
    cursor: pointer;
}

.bar {
    display: block;
    width: 25px;
    height: 3px;
    margin: 5px auto;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
    background-color: #fff;
}

@media (max-width: 768px) {
    .navbar {
        width: auto;
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
        flex-direction: column;
        background-color: rgba(103, 162, 240, 0.377);
        width: 100%;
        text-align: center;
        transition: 0.3s;
    }

    .nav-item {
        margin: 16px;
    }

    .nav-menu.active {
        right: 0;
    }
}
</style>