<template>
    <section>
        <div v-for="video in videos" :key="video.channelName">
            <img :src="video.thumbnail" alt="" />
        </div>
    </section>
</template>

<script setup>
defineProps({
    videos: {
        type: Array,
        default: () => [],
    },
})
</script>
