<template>
    <section class="about">
        <div class="about_area">
            <div class="about_content">
                <div class="about_img" data-aos="fade-right" data-aos-duration="1000">
                    <img class="" src="../assets/images/galib.jpg" alt="">
                </div>

                <div class="main_title" data-aos="fade-left" data-aos-duration="1000">
                    <h2>let’s Introduce about myself</h2>
                    <p>
                        I thrive on challenges! As a dedicated web application designer and
                        front-end developer, I see working under pressure as an opportunity to
                        excel. I'm passionate about <span> HTML, CSS, SCSS, Bootstrap, Tailwind CSS,
                            JavaScript, Vue.js, Nuxt.js,</span> and more, using my skills to create
                        engaging
                        digital experiences.

                    </p>
                    <p>
                        Feel free to connect with me for intriguing Web design discussions,
                        project collaborations, or to simply share a good book recommendation!.
                    </p>
                    <a class="btn" href="#"><span>Download CV</span></a>
                </div>
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
.about {
    background: rgb(51, 72, 133);
    padding: 40px 0;
}

.about_area {
    width: 80%;
    margin: 0 auto;
}

.about_content {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.about_content .about_img {
    width: 30%;
}

.about_content .about_img img {
    width: 300px;
    border-radius: 5px;
}


.about_content .main_title {
    width: 50%;
    color: #fff;
}

.about_content .main_title h2 {
    font-size: 30px;
    font-weight: bold;
    padding-bottom: 15px;
}

.about_content .main_title p {
    font-size: 16px;
    padding-bottom: 15px;
}

.about_content .main_title p span {
    font-size: 18px;
    font-weight: bold;
}

.about_content .main_title .btn {
    display: inline-block;
    cursor: pointer;
    padding: 10px 20px;
    border-radius: 5px;
    background-image: linear-gradient(to right, #4458dc 0%, #854fee 100%), radial-gradient(circle at top left, #4458dc, #854fee);
    box-shadow: 0px 10px 30px rgba(118, 85, 225, 0.3);
    transition: all ease-in-out .2s;
    text-decoration: none;
    color: #fff;
    cursor: pointer;
    font-size: 16px;
}

.about_content .main_title .btn:hover {
    transform: scale(1.1)
}

@media (max-width: 768px) {
    .about {
        padding: 40px 40px;
    }

    .about_area {
        width: auto;
    }

    .about_content {
        flex-direction: column;
    }

    .about_content .about_img {
        width: auto;
        padding-bottom: 20px;
    }

    .about_content .about_img img {
        width: 270px;
    }


    .about_content .main_title {
        width: auto;
    }

    .about_content .main_title h2 {
        line-height: 35px;
    }

    [data-aos] {
        opacity: 1 !important;
        transform: none !important;
        transition: none !important;
    }

}
</style>