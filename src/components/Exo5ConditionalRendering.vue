<script setup>
import { ref } from 'vue'

// Variable réactive pour l'état de connexion
const isLoggedIn = ref(false)

// Fonction pour basculer l'état
const toggleLogin = () => {
    isLoggedIn.value = !isLoggedIn.value
}

</script>

<template>
    <p v-if="isLoggedIn">Bienvenue utilisateur !</p>
    <p v-else>Veuillez vous connecter.</p>

    <button @click="toggleLogin">
        {{ isLoggedIn ? 'Se déconnecter' : 'Se connecter' }}
    </button>
</template>

<style scoped></style>
