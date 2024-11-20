<script setup lang="ts">
import { type RecipeResponse } from "../../types/types";

const { data, error } = await useFetch<RecipeResponse>("https://dummyjson.com/recipes?limit=12");
</script>

<template>
    <section class="py-10 container">
        <h1 class="text-3xl font-extrabold mb-6 text-balance border-b text-center">Découvrir, Créer, Partager</h1>
        <h2 class="text-lg lg:text-xl mb-12 text-center">Découvrez nos recettes les plus populaires !</h2>
        <div v-if="!error" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-4 gap-y-8">
            <RecipeCard v-for="recipe in data?.recipes" :recipe="recipe" />
        </div>
        <p v-else class="text-xl">Oups, une erreur s'est produite. Veuillez réessayer plus tard</p>
    </section>
</template>