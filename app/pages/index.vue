<script setup lang="ts">
//import { type RecipeResponse } from "../../types/types";
//const { data, error } = await useFetch<RecipeResponse>("https://dummyjson.com/recipes?limit=12");

useSeoMeta({
    title: "RecettesAMoi",
    description: "Des recettes à cuisiner !",
    ogTitle: "RecettesAMoi",
    ogDescription: "Des recettes à cuisiner !",
    ogImage: "/nuxt-course-hero.png",
    ogUrl: `http:localhost:3000`,
    twitterTitle: "RecettesAMoi",
    twitterDescription: "Des recettes à cuisiner !",
    twitterImage: "nuxt-course-hero.png",
    twitterCard: "summary",
});
</script>

<template>
    <main>
        <section class="bg-[#f1f1f1]">
            <div class="container flex flex-col lg:flex-row items-center py-10 gap-10">
                <div class="flex-1 order-2 lg:order-1 text-center lg:text-left">
                    <h1 class="text-3xl lg:text-5xl font-extrabold mb-6 text-balance">
                        Maîtrisez la cuisine en toute simplicité : libérez le chef qui sommeille en vous dès aujourd’hui !
                    </h1>
                    <p class="text-xl lg:text-2xl mb-8 text-balance">
                        Découvrez des recettes vous aidant à trouver la manière la plus simple de cuisiner.
                    </p>

                    <NuxtLink to="/recettes" class="px-4 py-2 text-white self-start bg-dodgeroll-gold rounded-md text-lg cursor-pointer">Parcourir toutes les recettes</NuxtLink>
                </div>
                <div class="flex-1 order-1 lg:order-2">
                    <NuxtImg sizes="xs:100vw sm:667px" src="/nuxt-course-hero.png" format="webp" densities="x1"
                        alt="" />
                </div>
            </div>
        </section>
        <!--
        <section class="py-20 container">
            <h2 class="text-3xl lg:text-4xl font-extrabold mb-2">Découvrir, Créer, Partager</h2>
            <p class="text-lg lg:text-xl mb-8">Découvrez nos recettes les plus populaires !</p>
            <div v-if="!error" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-x-4 gap-y-8">
                <RecipeCard v-for="recipe in data?.recipes" :recipe="recipe" />
            </div>
            <p v-else class="text-xl">Oups, une erreur s'est produite. Veuillez réessayer plus tard</p>
        </section>-->
    </main>
</template>

<style>
.main-container {
    height: calc(100vh - 90px);
}
</style>