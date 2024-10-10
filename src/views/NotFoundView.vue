<template>
    <section class="not-found">
        <div class="not-found-info">
            <i class="pi pi-exclamation-triangle"></i>
            <h1>404 Not Found</h1>
            <p class="text-xl mb-5">This page does not exist</p>
            <RouterLink to="/" class="back">Go Back
            </RouterLink>
        </div>
    </section>
</template>

<script setup>

</script>

<style scoped>
.not-found {
    background: #0630f080;
}

.not-found-info {
    width: 80%;
    height: 80vh;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 10px;
}

.not-found-info i {
    font-size: 50px;
    color: rgb(255, 0, 0);
}

.not-found-info h1 {
    font-size: 30px;
    color: #343434;
    line-height: 40px;
}

.not-found-info p {
    font-size: 16px;
    color: #343434;
    padding-bottom: 15px;
}

.not-found-info .back {
    text-decoration: none;
    font-size: 16px;
    color: #ffff;
    background: #01339e;
    padding: 10px 20px;
    border-radius: 8px;
    transition: all ease-in-out .3s;
}

.not-found-info .back:hover {
    transform: scale(1.08);
}
</style>