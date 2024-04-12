<script setup lang="ts">
import { ref } from 'vue'
const sectionOpen = ref(0)
</script>

<template>
<h1>Bonjour monde !</h1>

<section>
    <button class="text-xl" @pointerdown="sectionOpen = 1">bouton 1</button>
    <p v-show="sectionOpen === 1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto reiciendis necessitatibus, quas culpa aut qui officia cum aspernatur? Nostrum fugit facilis atque sunt provident consequatur omnis at minima vero nemo?</p>
</section>
<section>
    <button class="text-xl" @pointerdown="sectionOpen = 2">bouton 2</button>
    <p v-show="sectionOpen === 2">Maxime ullam commodi velit perferendis incidunt sapiente laudantium voluptates aperiam ad mollitia quo porro distinctio repudiandae soluta autem voluptas quod, possimus necessitatibus fugit quos. Soluta porro dicta voluptatibus eaque quod.</p>
</section>
<section>
    <button class="text-xl" @pointerdown="sectionOpen = 3">bouton 3</button>
    <p v-show="sectionOpen === 3">Cumque aspernatur repellat ea fugiat earum, dolorem iusto distinctio cupiditate quasi enim dolorum modi sunt assumenda quis, necessitatibus nulla obcaecati tempore est quo. Debitis recusandae dignissimos aliquam doloremque id aperiam.</p>
</section>

</template>
