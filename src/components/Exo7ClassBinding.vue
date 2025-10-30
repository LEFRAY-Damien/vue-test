<script setup>
import { ref } from 'vue'

// Variable booléenne réactive
const isActive = ref(false)

// Fonction pour basculer l’état
const toggleActive = () => {
    isActive.value = !isActive.value
}
</script>

<template>
    <button :class="{ active: isActive }" @click="toggleActive">
        {{ isActive ? 'Actif' : 'Inactif' }}
    </button>
</template>

<style scoped></style>