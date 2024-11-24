<script setup lang="ts">
import { type Recipe } from "../../types/types";

defineProps<{
    recipe: Recipe;
}>();
</script>

<template>
    <div id="recipes" class="shadow rounded-md">
        <!--Récupérer l'image depuis http://127.0.0.1:8000/uploads/img/recipes/ -->
        <NuxtImg sizes="xs:100vw sm:50vw md:50vw lg:50vw" format="webp" densities="x1" :src="`http://127.0.0.1:8000/uploads/img/recipes/${recipe.image}`" :alt="recipe.name" class="rounded-t-md" />
        <div class="flex flex-col py-6 px-4">
            <p class="text-2xl font-semibold mb-2">{{ recipe.name }}</p>
            <div class="font-normal w-full bg-white/80 flex gap-8 text-xl mb-4">
                <div class="flex items-center gap-1">
                    <Icon name="mdi:clock-time-eight-outline" style="color: #f79f1a" />
                    <span>{{ recipe.cookTimeMinutes }}</span>
                </div>
                <div class="flex items-center gap-1">
                    <Icon name="mdi:fire" style="color: #f79f1a" />
                    <span>{{ recipe.caloriesPerServing }}</span>
                </div>
                <div class="flex items-center gap-1">
                    <Icon name="mdi:star" style="color: #f79f1a" />
                    <span>{{ recipe.rating }} ({{ recipe.reviewCount }})</span>
                </div>
                <div class="flex items-center gap-1">
                    <Icon name="mdi:food-fork-drink" style="color: #f79f1a" />
                    <span>{{ recipe.servings }}</span>
                </div>
            </div>
            <BaseBtn :to="`/recipes/${recipe.id}`" label="Voir la recette" />
        </div>
    </div>
</template>

<style>
* {
    scroll-behavior: smooth;
}
</style>