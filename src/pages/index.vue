<script setup lang="ts">

import { ref } from 'vue';

  const maVar = ref(true)

</script>

<template>
  <button @click="maVar=!maVar">bouton cache</button>

  <h1 v-show="maVar" class="text-2xl">Bonjour monde !</h1>
</template>
