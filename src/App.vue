<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from '@/components/HelloWorld.vue'
</script>

<template>
  <div class="wrapper">
    <nav>
      <RouterLink to="/">Home</RouterLink>
      | 
      <RouterLink to="/about">About</RouterLink>
      | 
      <RouterLink to="/first">First Component</RouterLink>
    </nav>
  </div>

  <RouterView />
</template>

<style>

</style>
