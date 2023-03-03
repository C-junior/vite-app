<script setup>
const fe = defineProps(["name","imgSelFE","wt","weapon"])


</script>

<template>
    <div class="card" >
        <img :src="fe.imgSelFE" />    
  <div class="card-body">
    <h5 class="card-title text-center">{{ fe.name }}</h5>
    <hr>
    <div class="row">
        <section class="col">
            <span> Weapon:</span>
            <strong> {{ fe.wt }}</strong>
        </section>
        <section class="col">
            <span> Strong aganist:</span>
            <strong> Axe</strong>
        </section>
        <section class="col">
            <span> Weak aganist:</span>
            <strong> Lance</strong>
        </section>
             
    

    </div>
  </div>
</div>

</template>



<style>
</style>