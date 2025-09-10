<script setup>
import Main from '@/Main.vue'
import Nav from '@/Navbar.vue'
import Grid from '@/Grid.vue';
import {RouterView} from 'vue-router'
</script>

<template>
  <header>
 <Nav>
  </Nav>
  </header>

  <RouterView />
</template>

<style >


h1{
   font-size: clamp(2rem, 3.5vw, 3.8rem);
   margin-bottom: 1rem;
}
  p{
    font-size: clamp(1rem, 2.5vw, 2rem);
   
  }

  button {
    font-size: clamp(1rem, 2.5vw, 2rem);
  }

  code{
    letter-spacing: normal;
    font-size: clamp(1rem, 2.5vw, 2rem);
  }


</style>
