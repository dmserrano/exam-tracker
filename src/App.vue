<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="container mx-auto mt-4">
      <nav class="flex justify-around">
        <RouterLink to="/">Dashboard</RouterLink>
        <RouterLink to="/question/list">Question List</RouterLink>
      </nav>
    </div>
  </header>

  <div class="container mx-auto">
    <RouterView />
  </div>
</template>
