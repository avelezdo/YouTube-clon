<template>
    <section>
        <ItemVideo
            v-for="video in videos"
            :key="video.channelName"
            :video="video"
        ></ItemVideo>
    </section>
</template>

<script setup>
import ItemVideo from './VideoItem.vue'

defineProps({
    videos: {
        type: Array,
        default: () => [],
    },
})
</script>
