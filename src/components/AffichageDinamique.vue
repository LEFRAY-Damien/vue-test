<script setup>
import { ref } from 'vue'

// Variable booléenne
const actif = ref(false)

// Fonction pour changer l'état
const toggleActif = () => {
    actif.value = !actif.value
}
</script>

<template>
    <h2>État de l'utilisateur</h2>

    <!-- Bouton pour basculer l'état -->
    <button @click="toggleActif">
        {{ actif ? 'Désactiver' : 'Activer' }}
    </button>

    <!-- Message dynamique avec classe liée -->
    <p :class="actif ? 'actif' : 'inactif'">
        {{ actif ? 'Utilisateur actif' : 'Utilisateur inactif' }}
    </p>
</template>

<style scoped>
/* Classes CSS selon l’état */
.actif {
    color: green;
}

.inactif {
    color: red;
}
</style>