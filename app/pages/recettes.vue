<script setup lang="ts">
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
    <RecipesList />
</template>
