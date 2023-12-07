<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
      <nav>
        <RouterLink to="/" class="navbar-link">Home</RouterLink>
        <RouterLink to="/about" class="navbar-link">About</RouterLink>
      </nav>
  </header>
  <RouterView />
</template>

<style scoped>
header {
  width: 110%;
  right: -10%;
  height: 3rem;
  display: flex;
  background-color: rgb(145, 47, 145); 
  color: #fff;
  font-size: 1.5rem;
  padding-left: 1rem;
  position: fixed;
  top: 0;
  font-family: 'Caveat', cursive;
}
nav h1{
  color: #E9B0F5;
  transition: 0.7s;
}

nav h1:hover{
  color: #fff;
}
nav {
  column-gap: 2rem;
  margin-bottom: 0;
  display: flex;
  align-items: center;
}

.navbar-link {
  text-decoration: none;
  color: #fff;
  margin: 0 1rem; 
  transition: color 0.5s; 
}
.navbar-link:hover {
  color: #E9B0F5; 
}
</style>
