<script setup>
import { ref } from 'vue'

// Variable réactive pour le compteur
const compteur = ref(0)

// Fonctions pour les actions
const incrementer = () => {
    compteur.value++
}

const decrementer = () => {
    compteur.value--
}

const reinitialiser = () => {
    compteur.value = 0
}
</script>

<template>
    <h2>Mini Compteur</h2>

    <p class="valeur">Valeur actuelle : {{ compteur }}</p>

    <div class="boutons">
        <br>
        <button @click="incrementer">➕ Incrémenter</button>
        <br><br>
        <button @click="decrementer">➖ Décrémenter</button>
        <br><br>
        <button @click="reinitialiser">🔁 Réinitialiser</button>
    </div>
</template>

<style scoped></style>