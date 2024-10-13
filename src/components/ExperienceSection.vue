<template>
    <section class="experience" data-aos="fade-up" data-aos-anchor-placement="center-bottom"
        data-aos-duration="1500">
        <div class="title" data-aos="fade-right" data-aos-duration="1500">
            <h2>Work Experience</h2>
            <p>
                I worked as a Jr. Software Engineer at <span>Singularity Limited</span>. August 2021
                – May 2023.
            </p>
            <p>

                I was responsible for developing the front end of multiple websites, as well as
                maintaining and improving existing ones.
            </p>
        </div>
        <div class="projects" data-aos="fade-left" data-aos-duration="1500">

            <div class="project-item">
                <a href="https://ipdc.com/" target="_blank">
                    <img src="../assets/images/ipdc.png" alt="">
                </a>
                <a href="https://nagad.com.bd/" target="_blank">
                    <img src="../assets/images/nagad.png" alt="">
                </a>
                <a href="https://the-marvel.com/" target="_blank">
                    <img src="../assets/images/marvel-logo.png" alt="">
                </a>
            </div>
            <div class="technology">
                <p>
                    <span>Technologies Used : </span>SCSS, Bootstrap, JavaScript, Vue.js, Nuxt.js,
                    and Laravel.
                </p>
            </div>
        </div>
    </section>
</template>

<script setup>
import { onMounted } from "vue";
import AOS from "aos";

onMounted(() => {
    AOS.init();
})
</script>

<style scoped>
.experience {
    width: 80%;
    margin: 0 auto;
    padding: 40px 0;
}

.title {
    text-align: center;
    color: #343434;
    padding-bottom: 30px;
}

.title h2 {
    font-size: 30px;
    font-weight: bold;
}

.title p {
    font-size: 16px;
}

.title p span {
    font-weight: bold;
}

.projects {}


.project-item {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 40px;
}

.project-item a {}

.project-item a img {
    background: rgb(223, 226, 230);
    min-height: 88px;
    height: 70px;
    padding: 15px 20px;
    width: 150px;
    box-shadow: 0 0 10px #474444;
    border-radius: 8px;
    transition: all ease-in-out .3s;
}

.project-item a img:hover {
    transform: scale(1.07);
}

.technology p {
    text-align: center;
    font-size: 16px;
    padding-top: 15px;
    color: #343434;
}

.technology p span {
    font-weight: bold;
}

@media (max-width: 768px) {
    .experience {
        width: auto;
        padding: 30px 40px;
    }

    .title {
        padding-bottom: 30px;
    }

    .title h2 {
        font-size: 24px;
    }

    .title p {
        font-size: 14px;
    }

    .project-item {
        gap: 20px;
    }

    .technology p {
        font-size: 14px;
    }

    [data-aos] {
        opacity: 1 !important;
        transform: none !important;
        transition: none !important;
    }
}
</style>