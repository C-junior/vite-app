<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header >
    <nav class="navbar navbar-expand-lg  bg-white ">
  <div class="container-fluid all">
    <a class="navbar-brand" href="#">
      <img src="../src/assets/logofe.png " alt="Logo" width="30" height="30" class="d-inline-block align-text-top">
      Fire Emblem Fates Companion
    </a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse  " id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <RouterLink class="nav-link" to="/">Home</RouterLink>
        </li>       
        <li class="nav-item">
          <RouterLink class="nav-link" to="/about">About</RouterLink>          
        </li>
      </ul>
    </div>
  </div>
</nav>

    <!-- <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div> -->    
  </header>
  <main>
    
  </main>

  <RouterView />
<footer class="bg-danger">
  <div>
    Khaos Corp. {{ new Date().getFullYear() }}
  </div>
</footer>

  
</template>

<style scoped>

  footer{
  position: fixed;
  z-index: 99;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 56px;
  color: white;
display: flex;
justify-content: center;
align-items: center;
}

.all{
  width: 100vw ;
}

</style>
