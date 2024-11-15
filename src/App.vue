<script setup>
import { ref } from 'vue'

const uToC = ref(0)
const cToU = ref(0)

function usdToCAD(e, v = +e.target.value) {
  uToC.value = v
  cToU.value = //Need to add formula
}

function cadToUSD(e, v = +e.target.value) {
  cToU.value = v
  uToC.value = //Need to add formula
}
</script>

<template>

  <main>
    <input type="number" :value="uToC" @change="usdToCAD"> USD
    <input type="number" :value="cToU" @change="cadToUSD"> CAD
  </main>

</template>
