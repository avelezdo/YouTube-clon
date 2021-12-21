<template>
    <section class="p-2 flex overflow-scroll">
        <Chip
            text="Todo"
            :is-selected="isAllSelected"
            @click="selectCategory(0)"
        ></Chip>
        <Chip
            v-for="category in categories"
            :key="category.id"
            :text="category.name"
            :is-selected="checkIfIsSelected(category.id)"
            @click="selectCategory(category.id)"
        ></Chip>
    </section>
</template>

<script setup>
import Chip from './Chip.vue'
import { computed, ref } from '@vue/reactivity'

const emits = defineEmits(['select-category'])
const selectedCategory = ref()
const isAllSelected = computed(() => {
    return !selectedCategory.value
})
const checkIfIsSelected = categoryId => {
    return selectedCategory.value === categoryId
}
const selectCategory = categoryId => {
    selectedCategory.value = categoryId
    emits('select-category', categoryId)
}

defineProps({
    categories: {
        type: Array,
        default: () => [],
    },
})
</script>
