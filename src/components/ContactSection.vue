<template>
    <section>
        <div class="contact">
            <div class="contact-inner">
                <div class="contact-area" data-aos="zoom-out" data-aos-duration="1000">
                    <div class="title">
                        <h2>Contact Me</h2>
                        <p>
                            If you have any questions or need further information, please feel free
                            to reach out to me at this email address and Phone number.
                        </p>
                    </div>
                    <div class="contact-info">
                        <a href="#">
                            <span class="icon"><i class="pi pi-home"></i></span>
                            <p class="text">Mohammadia Housing
                                Society-8, Road 8/B,
                                H/5, Mohammadpur,
                                Dhaka-1207 Bangladesh.</p>
                        </a>
                        <a href="tel:+8801710571239">
                            <span class="icon"><i class="pi pi-phone"></i></span>
                            <p class="text">
                                +8801710571239
                            </p>
                        </a>
                        <a href="mailto:ashadullaalgalib@gmail.com">
                            <span class="icon"><i class="pi pi-inbox"></i></span>
                            <p class="text">
                                ashadullaalgalib@gmail.com
                            </p>
                        </a>

                    </div>
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
.contact {
    background: rgb(48, 80, 150);
    padding: 40px 0;
}

.contact-inner {
    width: 80%;
    margin: 0 auto;
}


.title {
    text-align: center;
    width: 500px;
    margin: 0 auto;
}

.title h2 {
    font-size: 30px;
    color: #fff;
    font-weight: bold;
}

.title p {
    font-size: 16px;
    color: #fff;
}

.contact-info {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-top: 40px;
}

.contact-info a {
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: 10px;
    width: 25%;
}

.contact-info a .icon {
    padding: 16px 18px;
    background: rgb(26, 41, 71);
    border-radius: 100%;
    transition: all ease-in-out .2s;
}


.contact-info a .icon:hover {
    padding: 18px 20px;
}

.contact-info a .icon i {
    color: #fff;
    font-size: 20px;
}

.contact-info a .text {
    color: #fff;
    font-size: 15px;
}

@media (max-width: 768px) {
    .contact {
        padding: 40px;
    }

    .contact-inner {
        width: auto;
    }

    .title {
        width: auto;
    }

    .title h2 {
        font-size: 24px;
    }

    .title p {
        font-size: 14px;
    }

    .contact-info {
        flex-direction: column;
        gap: 20px;
        padding-top: 25px;
    }

    .contact-info a {
        gap: 10px;
        width: auto;
        flex-direction: column;
    }

    .contact-info a .icon {
        padding: 14px 16px;
    }


    .contact-info a .icon:hover {
        padding: 16px 18px;
    }


    .contact-info a .text {
        font-size: 12px;
        text-align: center;
    }
}
</style>