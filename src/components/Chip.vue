<template>
    <div class="my-2 mr-2 text-sm" @click="emitClickEvent">
        <span class="chip border p-2 rounded-full" :class="chipClasess">{{
            text
        }}</span>
    </div>
</template>

<script setup>
import { computed } from '@vue/reactivity'

const emits = defineEmits(['click'])
const emitClickEvent = () => {
    emits('click')
}

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

<style scoped>
.chip {
    border-color: rgba(0, 0, 0, 0.1);
    background-color: rgb(0 0 0 / 5%);
}
.chip.selected {
    background-color: #606060;
    color: white;
}
</style>
