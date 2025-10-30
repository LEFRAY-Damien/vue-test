<script setup>
import { ref } from 'vue'

// Déclare une variable réactive pour le champ de texte
const nom = ref('')

</script>

<template>
    <input v-model="nom" type="text" placeholder="Entre ton nom ici" />
    <p>Tu as écrit : {{ nom }}</p>
</template>

<style scoped></style>
