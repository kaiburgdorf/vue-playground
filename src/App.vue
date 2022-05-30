<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <div class="wrapper">
    <b-nav tabs fill justified>
      <b-nav-item><RouterLink to="/">Home</RouterLink></b-nav-item>
      <b-nav-item><RouterLink to="/first">First Component</RouterLink></b-nav-item>
      <b-nav-item><RouterLink to="/about">About</RouterLink></b-nav-item>
    </b-nav>
  </div>

  <RouterView />
</template>

<style></style>
