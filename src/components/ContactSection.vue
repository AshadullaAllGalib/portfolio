<template>
    <section>
        <div class="contact">
            <div class="contact-inner">
                <div class="contact-area">
                    <div class="title">
                        <h2>Contact Me</h2>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At voluptates,
                            modi
                            facilis excepturi facere est natus accusantium doloribus, .
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

.contact-area {}

.title {
    text-align: center;
    width: 500px;
    margin: 0 auto;
}

.title h2 {
    font-size: 30px;
    color: #fff;
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
</style>