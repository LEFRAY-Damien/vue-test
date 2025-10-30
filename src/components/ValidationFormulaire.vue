<script setup>
import { ref } from 'vue'

// Champs et messages
const nom = ref('')
const message = ref('')
const erreur = ref(false)

// Fonction de validation
const envoyer = () => {
    if (nom.value.trim() === '') {
        erreur.value = true
        message.value = ''
    } else {
        erreur.value = false
        message.value = `Merci ${nom.value} !`
    }
}
</script>

<template>
    <h2>Formulaire avec validation</h2>

    <input type="text" v-model="nom" placeholder="Entrez votre nom" />
    <button @click="envoyer">Envoyer</button>

    <!-- Message d’erreur ou de succès -->
    <p v-if="erreur" class="erreur">Entrer votre nom !</p>
    <p v-else-if="message" class="message">{{ message }}</p>
</template>

<style scoped>
.erreur {
  color: red;
  font-weight: bold;
  margin-top: 15px;
}

.message {
  color: green;
  font-weight: bold;
  margin-top: 15px;
}
</style>
