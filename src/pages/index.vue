<script setup lang="ts">

import { ref } from 'vue';

  const maVar = ref(true)

</script>

<template>
  <button @click="maVar=!maVar">le crane de pratch</button>

  <h1 v-show="maVar" class="text-2xl">BIG CALVAS</h1>
</template>
