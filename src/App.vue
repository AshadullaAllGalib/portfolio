<script setup>
import Navbar from '@/components/NavBar.vue'
import FooterSection from './components/FooterSection.vue';
import { RouterView } from 'vue-router'
</script>

<template>
  <Navbar />
  <RouterView />
  <FooterSection />
</template>

<style scoped></style>
