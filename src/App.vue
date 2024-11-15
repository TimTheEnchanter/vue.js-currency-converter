<script setup>
import { ref } from 'vue'

const uToC = ref(0)
const cToU = ref(0)

function usdToCAD(e, v = +e.target.value) {
  uToC.value = v
  cToU.value = v * 1.4080534 //Nov 15 Rate
}

function cadToUSD(e, v = +e.target.value) {
  cToU.value = v
  uToC.value = v * 0.71015842 //Nov 15 Rate
}
</script>

<template>

  <main>
    <input type="number" :value="uToC" @change="usdToCAD"> USD
    <input type="number" :value="cToU" @change="cadToUSD"> CAD
  </main>

</template>
