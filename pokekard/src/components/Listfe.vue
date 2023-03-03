<script setup >

const fe = defineProps(["feChar", "feImg", "feWt"])
</script>


<template>

<div class=" col-4">
<div class="card lista mb-3 ">
   
     <!--<li class="" v-for="fe in fes"
      :key="fe.name"
      >
         <img :src="imageUrl" alt="" width="150px"> -->
         
        
         <img :src="fe.feImg" />    
         
         <br>
         {{ fe.feChar }}
        <br>
        {{ fe.feWt }}
        
       
        
    
</div>

</div>
</template>
<style>
.card {
    color: black;
  
    justify-content: end;
    width: 100%;    
    
}

.lista {
    height: 200px;
    
}
.lista img {
    max-height: 150px;
}

</style>