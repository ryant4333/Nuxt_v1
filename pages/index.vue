<template>  
  <main>
    <h3>Home Page</h3>
    <NuxtLink to="/">Home Page</NuxtLink>
    <NuxtLink to="/about">About page</NuxtLink> 

    <landing />

    <hero />


  </main>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  asyncData() {
    return {
      rendering: process.server ? 'server' : 'client'
    }
  }
})
</script>
