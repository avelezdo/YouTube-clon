<template>
    <span class="chip" :class="chipClasess">{{ text }}</span>
    <!-- <span class="chip" :class="isSelected ? 'selected' : ''">{{ text }}</span> -->
</template>

<script setup>
import { computed } from '@vue/reactivity'
const props = defineProps({
    text: {
        type: String,
        required: true,
    },
    isSelected: {
        type: Boolean,
        default: false,
    },
})

const chipClasess = computed(() => {
    return { selected: props.isSelected }
})
</script>
