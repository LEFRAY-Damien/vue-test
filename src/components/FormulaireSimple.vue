<script setup>
import { ref } from 'vue'

// Champs liés au formulaire
const nom = ref('')
const email = ref('')
const message = ref('')

// Fonction appelée lors de la soumission
const inscrire = () => {
    message.value = `Bienvenue, ${nom.value} ! Votre email ${email.value} a été enregistré.`
}

</script>

<template>
    <h2>Formulaire d'inscription</h2>

    <form @submit.prevent="inscrire">
        <input type="text" v-model="nom" placeholder="Entrez votre nom" required />
        <input type="email" v-model="email" placeholder="Entrez votre email" required />
        <button type="submit">S'inscrire</button>
    </form>

    <!-- Message affiché après soumission -->
    <p v-if="message" class="message">{{ message }}</p>
</template>

<style scoped></style>