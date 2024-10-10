<template>
    <button v-if="isVisible" @click="scrollToTop" class="back-top">
        ↥
    </button>
</template>
<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
const isVisible = ref(false);
const handleScroll = () => {
    isVisible.value = window.scrollY > 300;
}
const scrollToTop = () => {
    window.scrollTo({ top: 0, behavior: 'smooth' })
}
onMounted(() => {
    window.addEventListener('scroll', handleScroll)
});

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
})
</script>
<style scoped>
.back-top {
    display: flex;
    position: fixed;
    right: 1rem;
    bottom: 1rem;
    justify-content: center;
    align-items: center;
    border-radius: 100%;
    width: 3.5rem;
    height: 3.5rem;
    font-size: 1.25rem;
    line-height: 1.75rem;
    color: #ffffff;
    background-color: #1d2947;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    transition-duration: 300ms;
    transition-duration: 300ms;
    cursor: pointer;
    border: none;
    transition: all ease-in-out .3s;
}

.back-top:hover {
    transform: scale(1.08);
}
</style>
