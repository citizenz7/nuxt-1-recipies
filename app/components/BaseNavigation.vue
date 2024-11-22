<script setup lang="ts"></script>

<template>
  <header class="py-4 border-b">
    <nav class="flex container items-center">
      <NuxtLink to="/" class="flex gap-1 items-center">
        <NuxtImg width="56px" format="webp" densities="x1" src="/icon-green.png" alt="ImageLogo" />
        <span class="font-bold main-title">RecettesAMoi</span>
      </NuxtLink>
      <ul class="flex gap-6 ml-auto text-xl font-bold capitalize">
        <li>
          <NuxtLink to="/">Accueil</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/recettes">Recettes</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about">A propos</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/contact">Contact</NuxtLink>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style>
  .main-title {
    font-size: clamp(20px, 2vw, 32px);
    font-weight: 700;
  }
</style>