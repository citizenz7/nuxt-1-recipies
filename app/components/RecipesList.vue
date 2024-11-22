<script setup lang="ts">
import { type RecipeResponse } from "../../types/types";

// const { data, error } = await useFetch<RecipeResponse>("http://127.0.0.1:8000/api/recipes");
const { data, status, error, refresh, clear, pending } = await useAsyncData(
    'recipes',
  () => $fetch('http://127.0.0.1:8000/api/recipes'),
)
// console.log(error);
</script>

<template>
    <section class="py-10 container">
        <h1 class="text-3xl font-extrabold mb-6 text-balance border-b text-center">Découvrir, Créer, Partager</h1>
        <h2 class="text-lg lg:text-xl mb-12 text-center">Découvrez nos recettes les plus populaires !</h2>
        <div v-if="!error" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-4 gap-y-8">
            <RecipeCard v-for="recipe in data" :recipe="recipe" />
        </div>
        <p v-else class="text-xl text-center text-red-500 border-2 p-3">
            {{ error }}<br>
            {{ pending }}
        </p>
    </section>
</template>