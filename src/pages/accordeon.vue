<script setup lang="ts">

import { ref } from 'vue';

  const maVar = ref(1)

  const sectionOpen = ref(0)


</script>

<template>


    <section class=" flex flex-col justify-center items-center">
            <button class="text-xl rounded-full border-2 border-red-600 bg-red-300 px-2" @pointerdown="sectionOpen = sectionOpen === 1 ? 0 : 1 ">bouton 1</button>
    </section>
    <p v-show="sectionOpen === 1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet ad molestiae unde debitis aperiam quaerat consectetur, nulla, facere nisi voluptatum explicabo adipisci optio? Magnam unde inventore quas ratione dolore nostrum.</p>

<section class="flex flex-col justify-center items-center">
    <button class="text-xl rounded-full border-2 border-red-600 bg-red-300 px-2" @pointerdown="sectionOpen = sectionOpen === 2 ? 0 : 2 " >bouton 2</button>
    <p v-show="sectionOpen === 2">Reiciendis deserunt nobis quos, eveniet iusto inventore consequuntur eos, voluptatibus magni dicta accusamus alias optio reprehenderit ratione quo modi doloremque soluta placeat voluptate repudiandae eaque praesentium. Vel non distinctio tempore.</p>
  </section>
  <section class="flex flex-col justify-center items-center">
    <button class="text-xl rounded-full border-2 border-red-600 bg-red-300 px-2 " @pointerdown="sectionOpen = sectionOpen === 3 ? 0 : 3">bouton 3</button>
    <p v-show="sectionOpen === 3">Obcaecati, et accusantium? Quaerat dolore fuga reprehenderit nemo inventore? Ex veritatis repellat delectus quo nostrum reprehenderit inventore quisquam architecto id non quos mollitia, minus tenetur neque! Ex quam pariatur voluptatum.</p>
  </section>


  

</template>