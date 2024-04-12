<script setup lang="ts">
import { onErrorCaptured } from 'vue'
import { RouterLink, RouterView } from 'vue-router/auto'

import { ref } from 'vue'
const menuIsOpen = ref(false)

onErrorCaptured((err, instance, info) => {
  console.error('erreur : ', err, '\ninfo : ', info, '\ncomposant : ', instance)
  return true
})

</script>

<template>

<button
  @pointerdown="menuIsOpen = !menuIsOpen"
  aria-controls="mainNav"
  aria-expanded="true"
  class="rounded-full border-2 border-red-600 bg-red-300 px-2"
>
  menu
</button>
<!-- nav#mainNav>ul>li*3>a[href="#"]{item $} -->
<Transition
  class="transition-transform duration-1000"
  enter-from-class="-translate-x-full"
  enter-to-class="translate-x-0"
  leave-active-class="-translate-x-full"
>
<nav id="mainNav"  v-show="menuIsOpen === true">
  
  <ul>
    <li><a href="#"><RouterLink to="/" class="text-red-500 underline"> Accueil </RouterLink></a></li>
    <li><a href="#"><router-link to="/accordeon" class="text-red-500 underline"> Accordeon </router-link></a></li>
    <li><a href="#">item 3</a></li>
  </ul>
</nav>
</Transition>

  <header>
    
    
  </header>
  <main>
    
  </main>
  <RouterView v-slot="{ Component }">
    <Suspense>
      <component :is="Component" />
    </Suspense>
  </RouterView>

  
</template>
