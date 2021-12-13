<template>
    <section><Chip text="Todo" is-selected="true"></Chip></section>
    <section>
        <Chip
            v-for="category in categories"
            :key="category.id"
            :text="category.name"
        ></Chip>
    </section>
</template>

<script setup>
import Chip from './Chip.vue'
defineProps({
    categories: {
        type: Array,
        default: () => [],
    },
})
</script>
