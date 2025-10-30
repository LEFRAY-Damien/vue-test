<script setup>
import { ref } from 'vue'

// Liste des tâches et champ de saisie
const taches = ref([])
const nouvelleTache = ref('')

// Fonction d’ajout
const ajouterTache = () => {
    if (nouvelleTache.value.trim() !== '') {
        taches.value.push(nouvelleTache.value.trim())
        nouvelleTache.value = '' // réinitialiser le champ
    }
}

</script>

<template>
    <h2>Ma TODO List</h2>

    <div class="input-section">
        <input v-model="nouvelleTache" type="text" placeholder="Entrez une tâche..." />
        <button @click="ajouterTache">Ajouter</button>
    </div>

    <!-- Affiche un message si aucune tâche -->
    <p v-if="taches.length === 0">Aucune tâche</p>

    <!-- Liste des tâches -->
    <ul v-else>
        <li v-for="(tache, index) in taches" :key="index">
            {{ tache }}
        </li>
    </ul>
</template>

<style scoped></style>