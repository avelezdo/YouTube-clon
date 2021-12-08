<script setup>
import BaseHeader from './components/BaseHeader.vue'
import VideosList from './components/VideosList.vue'
import { videos } from './assets/videos.json'
console.log(videos)
</script>

<template>
    <BaseHeader></BaseHeader>
    <VideosList :videos="videos" />
</template>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    /* color: #2c3e50; */
}
</style>
