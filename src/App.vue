<script setup>
// importando funcion para crear referncias reactivas
import {ref} from 'vue'
// creando una referencia reactiva de tipo string
const header = ref('App lista de compras');
const shoppingIcons =('material-icons shopping-cart-icon')
</script>

<template>
  <h1><i v-bind:class="shoppingIcons">local_mall</i>{{header}}</h1>
</template>

<style scoped>
.shopping-cart-icon{
  font-size:  2rem;
}
</style>

