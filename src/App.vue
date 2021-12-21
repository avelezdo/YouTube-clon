<script setup>
import { ref } from '@vue/reactivity'
import BaseHeader from './components/BaseHeader.vue'
import VideosList from './components/VideosList.vue'
import CategoriesList from './components/CategoriesList.vue'
import { videos } from './assets/videos.json'

let filteredVideos = ref(videos)
import { categories } from './assets/categories.json'

const selectVideosWithCategory = categoryId => {
    filteredVideos.value =
        categoryId === 0
            ? videos
            : videos.filter(v => v.category === categoryId)
}
</script>

<template>
    <BaseHeader></BaseHeader>
    <CategoriesList
        :categories="categories"
        @select-category="selectVideosWithCategory"
    ></CategoriesList>
    <VideosList :videos="filteredVideos" />
</template>
