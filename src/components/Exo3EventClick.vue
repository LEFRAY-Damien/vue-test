<script setup>
import { ref } from 'vue'

// Déclare une variable réactive pour compter les clics
const count = ref(0)

// Fonction pour incrémenter le compteur
const increment = () => {
  count.value++
}

</script>

<template>
    <button @click="increment">Clique-moi</button>
    <p>Nombre de clics : {{ count }}</p>
</template>

<style scoped></style>
