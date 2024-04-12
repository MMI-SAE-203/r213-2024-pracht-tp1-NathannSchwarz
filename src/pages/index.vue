<script setup lang="ts">

import { ref } from 'vue';

  const maVar = ref(1)

  const sectionOpen = ref(0)

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

  <section>
   
    <button class="text-xl" @pointerdown="sectionOpen = sectionOpen === 1 ? 0 : 1 ">bouton 1</button>
    <p v-show="sectionOpen === 1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet ad molestiae unde debitis aperiam quaerat consectetur, nulla, facere nisi voluptatum explicabo adipisci optio? Magnam unde inventore quas ratione dolore nostrum.</p>
  </section>
  <section>
    <button class="text-xl" @pointerdown="sectionOpen = sectionOpen === 2 ? 0 : 2 " >bouton 2</button>
    <p v-show="sectionOpen === 2">Reiciendis deserunt nobis quos, eveniet iusto inventore consequuntur eos, voluptatibus magni dicta accusamus alias optio reprehenderit ratione quo modi doloremque soluta placeat voluptate repudiandae eaque praesentium. Vel non distinctio tempore.</p>
  </section>
  <section>
    <button class="text-xl" @pointerdown="sectionOpen = sectionOpen === 3 ? 0 : 3">bouton 3</button>
    <p v-show="sectionOpen === 3">Obcaecati, et accusantium? Quaerat dolore fuga reprehenderit nemo inventore? Ex veritatis repellat delectus quo nostrum reprehenderit inventore quisquam architecto id non quos mollitia, minus tenetur neque! Ex quam pariatur voluptatum.</p>
  </section>


  <section v-for="({ label, texte }, key) of sectionsData" :key="key">
        <pre class="font-mono">key : {{ key }}</pre>
        <pre @pointerdown="sectionOpen1 = sectionOpen1 === key ? 50 : key" class="font-mono">label : {{ label }}</pre>
        <pre  v-show="sectionOpen1 === key" class="font-mono">texte : {{ texte }}</pre>
    </section>

</template>
