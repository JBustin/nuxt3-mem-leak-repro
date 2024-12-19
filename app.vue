<template>
  <div>
    <NuxtRouteAnnouncer />
    <NuxtWelcome />
  </div>
</template>

<script setup lang="ts">
const config = useRuntimeConfig()
// persistent duplicated public apiKey in memory, one by code execution
console.log(config)

// no duplicates
const test = { value: 'COUCOU' }
console.log(test)
</script>
