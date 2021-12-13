<script setup>
import BaseHeader from './components/BaseHeader.vue'
import VideosList from './components/VideosList.vue'
import CategoriesList from './components/CategoriesList.vue'
import { videos } from './assets/videos.json'
import { categories } from './assets/categories.json'
</script>

<template>
    <BaseHeader></BaseHeader>
    <CategoriesList :categories="categories"></CategoriesList>
    <VideosList :videos="videos" />
</template>
