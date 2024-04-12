<script setup lang="ts">

import { ref } from 'vue';

  const maVar = ref(1)


</script>

<template>
  <p>mavar : {{ maVar }}</p>

  <button @click="maVar = maVar === 1 ? 0 : 1">bouton</button>
  
  <h1 v-show="maVar === 1" class="text-2xl">maVAr vaut 1 !</h1>

  <button @click="maVar = maVar === 2 ? 0 : 2">bouton 2</button>

  <h1 v-show="maVar === 2" class="text-2xl">maVAr vaut 2 !</h1>




</template>
