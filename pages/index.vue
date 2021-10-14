<template>  
  <main>
    <h3>Home Page</h3>
    <NuxtLink to="/">Home Page</NuxtLink>
    <NuxtLink to="/about">About page</NuxtLink> 

    <p>
      This page is rendered on the <strong>{{ rendering }}</strong>
    </p>
    <p v-if="rendering === 'server'">
      First load or hard refresh is done server side.
    </p>
    <p v-if="rendering === 'client'">
      Navigation done on client side
    </p>

    <NuxtLink to="/about">About Page</NuxtLink>
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
