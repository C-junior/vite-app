<script setup>
import {onMounted, reactive, ref} from "vue"

const datab = 

onMounted(()=>{
  fetch("/src/ ")
  .then(res => res.json())
  .then(res => console.log(res))
  
})

</script>

<template>
  <main>
    <div class="container text-center">
  <div class="row">
    <div class="col-sm-12 col-md-6">
      <div class="card mt-4" style="width: 18rem;">
  <img src="https://cdn.w1st.xyz/cards/characters/53dac56c-0d15-4101-9e91-e4601cc19f12.jpg" class="card-img-top" alt="...">
  
</div>
    </div>
    <div class="col-sm-12 col-md-6">
    <ul>
     <!-- <li v-for="fgo in fgos"
      :key="fgo.name"
      >
        {{ fgo.name }}
        <br>
      
      </li>  -->
    </ul>
    </div>
    <div class="col-sm-12 col-md-6">
      Column
    </div>
  </div>
</div>
  </main>
</template>
