<template>
    <section class="home_banner_area">
        <div class="banner_inner">

            <div class="banner_content" data-aos="fade-up" data-aos-duration="1000">
                <h3 class="text-uppercase">HELLO</h3>
                <h1 class="text-uppercase">I AM ASHADULLA ALL GALIB</h1>
                <h5 class="text-uppercase">FRONT-END DEVELOPER</h5>
                <div class="download-btn">
                    <a href="../assets/images/cv.pdf" download="cv.pdf"><span>Get CV</span></a>
                </div>
            </div>

            <div class="home_right_img" data-aos="fade-down" data-aos-duration="1000">
                <img class="" src="../assets/images/hero-right.png" alt="">
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
.home_banner_area {
    width: 80%;
    margin: 0 auto;
    padding-top: 100px;
}

.banner_inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.banner_content h3 {
    font-size: 40px;
    margin-bottom: 15px;
    position: relative;
    color: #000000;
}

.banner_content h3::after {
    content: "";
    width: 200px;
    height: 2px;
    position: absolute;
    top: 50%;
    left: 25%;
    background: #000000;
}

.banner_content h1 {
    font-size: 40px;
    margin-bottom: 15px;
    font-weight: bold
}

.banner_content h5 {
    font-size: 24px;
    margin-bottom: 25px;
}

.banner_content .download-btn {
    display: inline-block;
    cursor: pointer;
    padding: 10px 20px;
    border-radius: 5px;
    background-image: linear-gradient(to right, #4458dc 0%, #854fee 100%), radial-gradient(circle at top left, #4458dc, #854fee);
    box-shadow: 0px 10px 30px rgba(118, 85, 225, 0.3);
    transition: all ease-in-out .2s;
}

.banner_content .download-btn:hover {
    transform: scale(1.1);
}

.banner_content .download-btn a {
    color: #ffff;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 20px;
}

.home_right_img {}

.home_right_img img {
    width: 400px;
}

@media (max-width: 768px) {
    .home_banner_area {
        width: auto;
    }

    .banner_inner {
        flex-direction: column;
        padding: 0 40px;
    }

    .banner_content {
        padding-bottom: 30px;
    }

    .banner_content h3 {
        font-size: 30px;
        margin-bottom: 0;
    }

    .banner_content h3::after {
        width: 150px;
        left: 40%;
    }

    .banner_content h1 {
        font-size: 18px;
        margin-bottom: 5px;
        font-weight: bold
    }

    .banner_content h5 {
        font-size: 20px;
        margin-bottom: 20px;
    }

    .banner_content .download-btn {

        padding: 8px 20px;
    }

    .banner_content .download-btn a {
        font-size: 16px;
    }

    .home_right_img img {
        width: 300px;
    }
}
</style>