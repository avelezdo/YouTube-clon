<template>
    <img :src="video.thumbnail" :alt="video.title" />
    <span>{{ video.duration }}</span>
    <div>
        <img
            :src="video.channelImg"
            :alt="`youtube channel ${video.channelName}`"
        />
    </div>
    <h4>{{ video.title }}</h4>
    <p>
        {{ `${video.channelName} ${video.visualizations} de ${video.date}` }}
    </p>
</template>

<script setup>
defineProps({
    video: {
        type: Object,
        default: () => {},
    },
})
</script>
