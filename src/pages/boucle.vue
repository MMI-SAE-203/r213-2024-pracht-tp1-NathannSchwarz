<script setup lang="ts">

import { ref } from 'vue';

  const sectionsData = [
  {
    label: 'bouton 1',
    texte: 'Bouton uno'
  },
  {
    label: 'bouton 2',
    texte: 'Ceci est le bouton 2 !'
  },
  {
    label: 'bouton 3',
    texte: 'Ceci est le bouton 3 !'
  }
]
const sectionOpen1 = ref(50)

</script>

<template>
    <section v-for="({ label, texte }, key) of sectionsData" :key="key">
        <pre class="font-mono">key : {{ key }}</pre>
        <pre @pointerdown="sectionOpen1 = sectionOpen1 === key ? 50 : key" class="font-mono">label : {{ label }}</pre>
        <pre  v-show="sectionOpen1 === key" class="font-mono">texte : {{ texte }}</pre>
    </section>
</template>