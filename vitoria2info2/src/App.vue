<script setup>
import { ref , computed } from 'vue'
const contador = ref (10)
function incrementar (){
  contador.value++
}
function decrementar(){
  if (contador.value > 0)
  contador.value--
}
function reset(){
  contador.value = 0
}

const contador2 = ref (10)
function incrementar2 (){
  contador2.value++
}
function decrementar2 (){
  if (contador2.value > 0)
  contador2.value--
}
function reset2 (){
  contador2.value = 0
}


</script>

<template>
  <button @click="incrementar">+</button>
  <button @click="decrementar">-</button>
  <button @click="reset">c</button>
  <p>Valor do contador: {{  contador + contador2 }}</p>
 
  <div class="info">
      Contador: {{  contador2 + contador }}
      <button @click="contador2++">+</button>
      <button @click="contador2--">-</button>
      <div v-if="contador2 > 10" class="verde">O contador é maior que 10</div>
      <div v-else-if="contador2 < 10" class="vermelho">O contador é menor que 10</div>
      <div v-else>O contador é 10</div>
      <hr />
      <div v-if="contador2 % 2 === 0">É par</div>
      <div v-else>É impar</div>
    </div>

</template>

<style scoped>
button {
  margin-left: 10px;
  background-color: rgb(23, 205, 230);
  color: black;
  border: none;
  border-radius: 5px;
  padding: 5px 10px;
  cursor: pointer;  
}</style>