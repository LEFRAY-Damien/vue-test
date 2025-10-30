<script setup>
import { ref } from 'vue'

// Tableau des produits
const produits = ref([
  { nom: 'Chaise', prix: 30 },
  { nom: 'Table', prix: 90 },
  { nom: 'Lampe', prix: 35 },
  { nom: 'Sofa', prix: 250 },
  { nom: 'Tapis', prix: 80 }
])

</script>

<template>
  <h2>Liste des produits</h2>

    <!-- Affichage des produits -->
    <div class="produits">
      <div class="carte" v-for="(produit, index) in produits" :key="index">
        <br>
        <p><strong>Produit :</strong> {{ produit.nom }}</p>
        <p><strong>Prix :</strong> {{ produit.prix }} €</p>
      </div>
    </div>
</template>

<style scoped>

</style>