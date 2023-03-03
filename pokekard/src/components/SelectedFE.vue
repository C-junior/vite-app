<script setup>
const fe = defineProps(["name","imgSelFE","wt","strong","weak"])

</script>

<template>
    <div class="feselect">
    <div 
    v-if="fe.wt === 'Sword || Katana'" class="card redbg" >
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
            <strong> {{fe.strong}}</strong>
        </section>
        <section class="col">
            <span> Weak aganist:</span>
            <strong> {{ fe.weak }}</strong>
        </section>
             
    

    </div>
  </div>
</div>

<div 
    v-else-if="fe.wt === 'Axe'" class="card greenbg" >
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
            <strong> {{fe.strong}}</strong>
        </section>
        <section class="col">
            <span> Weak aganist:</span>
            <strong> {{ fe.weak }}</strong>
        </section>
             
    

    </div>
  </div>
</div>

<div 
v-else-if="fe.wt === 'Lance || Spear'" class="card greenbg" >
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
            <strong> {{fe.strong}}</strong>
        </section>
        <section class="col">
            <span> Weak aganist:</span>
            <strong> {{ fe.weak }}</strong>
        </section>
             
    

    </div>
  </div>
</div>

<div 
    v-else
     class="card graybg" >
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
            <strong> {{fe.strong}}</strong>
        </section>
        <section class="col">
            <span> Weak aganist:</span>
            <strong> {{ fe.weak }}</strong>
        </section>
             
    

    </div>
  </div>
</div>

</div>
</template>



<style>
.feselect{
    max-height: 75vh;
  overflow-y: scroll;
  overflow-x: hidden;
}

.redbg{
    background-color: red;
}
.greenbg{
    background-color: green;
}

.bluebg{
    background-color: blue;
}
.graybg{
    background-color: rgb(111, 111, 116);
}


</style>