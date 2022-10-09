<script setup>
import { reactive, computed } from 'vue'

const author = reactive({
    name: 'John Doe',
    books: [
        'Vue 2',
        'Vue 3',
        'Vue 4'
    ]
})

// 一个计算属性 ref
const publishedBooksMessage = computed(() => {
    return author.books.length > 0 ? 'Yes' : 'No'
})
</script>

<template>
    <p>Has published books:</p>
    <span>{{ publishedBooksMessage }}</span>
</template>