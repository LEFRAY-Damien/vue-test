<script setup>
import { ref } from 'vue'

// Tableau réactif de fruits
const fruits = ref(['Pomme', 'Banane', 'Cerise'])

</script>

<template>
    <h2>Liste de fruits</h2>
    <ul>
        <li v-for="(fruit, index) in fruits" :key="index">
            {{ fruit }}
        </li>
    </ul>
</template>

<style scoped></style>