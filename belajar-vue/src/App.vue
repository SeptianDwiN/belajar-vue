<script setup>
import { ref } from 'vue'

const msg = "<h2>Hello World</h2>"
const link = "https://www.youtube.com/"
const number = prompt("Masukan Angka")
let a = 10
let b = 5
let c = a + b 
</script>

<template>
  <div >
    <span v-html="msg"></span> <!--menggunakan HTML yg ada di dalam variabel -->
    <span>{{ mesage }}</span>
    <a v-bind:href="link">youtube</a> <!--menggunakan atribut HTML ke VUE JS menggunakan v-bind-->
    <br>
  <button :disabled="IsButtonDisabble">Button</button>

  <br>
  bil a = {{ a }}
  <br>
  bil b = {{ b }}
  <br>
  hasil bil a + b ={{ c }}
  <br>

<p>{{ parseInt(number) }}</p>
<p>{{ number ? 'TRUE : 1 ' : 'FALSE : 0' }}</p>


  </div> 

</template>