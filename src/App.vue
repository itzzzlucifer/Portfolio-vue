<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
      <nav>
        <span>Aurum</span>
        <div id="navMid">
        <RouterLink class="navItem" to="/">Home</RouterLink>
        <RouterLink class="navItem" to="/about">About</RouterLink>
        <RouterLink class="navItem" to="/contacts">Contacts</RouterLink>
        </div>
      </nav>
      <header></header>
  <RouterView />
</template>

<style scoped>
</style>
