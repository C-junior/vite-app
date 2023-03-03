<script setup>
import {onMounted, reactive, ref, computed, watch} from "vue"
import Listfe from "../components/Listfe.vue";
import SelectedFE from "../components/SelectedFE.vue"


let fecharj = "../src/assets/fechars.json"
let fes = reactive(ref())
let fecharurl = "https://api.jsonbin.io/v3/b/63f927aeebd26539d084bb26"
let search = ref("")
let feSelected = reactive(ref())
let feW = feSelected.weapontype

onMounted(()=>{
  fetch(fecharurl)
  .then(res => res.json())
  .then(res => fes.value = res.record.characters)

})

const fesearch = computed (()=>{

  if (fes.value && search.value){
    return fes.value.filter(fe=> fe.name.includes(search.value)
    )
  }
  return fes.value

})

const selectFE = async (fe) => {  
  feSelected.value = fe

 
 
}

// function handleChange() {
//   const weapon = document.getElementById('weapon');
//   const chang = document.getElementById('search');
//   if ("Sword" === 'Sword') {
//     chang.style.backgroundColor = 'red';
//   } else {
//     chang.style.backgroundColor = '';
//   }
// }


// const weaponFe = computed (() =>{

//   weaponStrength(); {
//       let strength, weakness;

//       switch (this.feSelected.wt) {
//         case 'sword':
//           strength = 'axe';
//           weakness = 'lance';
//           break;
//         case 'axe':
//           strength = 'lance';
//           weakness = 'sword';
//           break;
//         case 'lance':
//           strength = 'sword';
//           weakness = 'axe';
//           break;
//         default:
//           strength = null;
//           weakness = null;
          
//       console.log(weaponFe)
//       }

//       return { strong: strength, weak: weakness }
//     }
   
//     // color() {
//     //   switch (this.selectedWeapon) {
//     //     case 'sword':
//     //       return 'red';
//     //     case 'axe':
//     //       return 'green';
//     //     case 'lance':
//     //       return 'blue';
//     //     default:
//     //       return 'black';
//     //   }
//     // },

// })

</script>


<template>
  <main class="container">



    <SelectedFE 
    :name="feSelected?.name"
    :imgSelFE="feSelected?.image"
    :wt="feSelected?.weapontype"
    :strong="feSelected?.strongvs"
    :weak="feSelected?.weakvs"
    />
   
    <div class="mb-3">
      <label hidden for="search"></label>
      <input 
      v-model="search"
      type="text" id="search" placeholder="Pesquisar..." style="width: 100%;">

    </div>
    <div class=" text-center card-list">
  <div class="row">    
    <div class="col-sm-12 col-md-12 "  >
      <div class="card-body row">
      <Listfe 
      v-for=" fe in fesearch"
      :key="fe.name"
      :feChar="fe.name"
      :feImg="fe.image"
      :feWt="fe.weapontype"
      @click="selectFE(fe)"
      />
    </div>
    </div>
   
  </div>
</div>
  </main>
</template>


<style>
.card-list{
  max-height: 75vh;
  overflow-y: scroll;
  overflow-x: hidden;
}

</style>
