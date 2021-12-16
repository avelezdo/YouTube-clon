<template>
    <div>
        <div class="relative">
            <img :src="video.thumbnail" :alt="video.title" />
            <span
                class="absolute bottom-0 right-0 bg-black m-2 p-0.5 text-white font-bold text-sm"
                >{{ video.duration }}</span
            >
        </div>
    </div>

    <div class="p-4 flex items-start">
        <img
            :src="video.channelImg"
            :alt="`youtube channel ${video.channelName}`"
            class="rounded-full w-10 h-10 mr-4"
        />
        <div>
            <h4 class="text-sm font-bold video-title">{{ video.title }}</h4>
            <p class="text-xs">
                {{
                    `${video.channelName} ${video.visualizations} de ${video.date}`
                }}
            </p>
        </div>
    </div>
</template>

<script setup>
defineProps({
    video: {
        type: Object,
        default: () => {},
    },
})
</script>

<style scoped>
.video-title {
    text-overflow: ellipsis;
    overflow: hidden;
    max-height: 2.5rem;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
}
</style>
