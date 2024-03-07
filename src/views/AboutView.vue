<script setup>
import { ref } from 'vue' 
let detik = ref(2)
const model = defineModel()

let mobil = ref({
  roda: 4,
  auto: true,
  warna: "Kuning"
})
function increment() {
  detik.value++
}

function gatiWarna() {
  mobil.value.warna = model.value
}

</script>

<template>
  <div>
    <input type="text" v-model="model"></input>
    <button @click=gatiWarna() >Ganti Warna </button>
    <br/>
    <p>Mobil saya berwarna {{ mobil.warna }}<br/>
    Rodanya <b>{{mobil.roda}}</b></p>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
