<script setup>
import HomeIntro from '~/components/HomeIntro.vue';
</script>

<template>
  <div class="bg-sky-900">
    <Navbar />
    <HomeIntro />
    <slot></slot>
  </div>
</template>

<style lang="css" scoped></style>
