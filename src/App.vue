<script setup>
// importando funcion para crear referncias reactivas
import {ref} from 'vue'
// creando una referencia reactiva de tipo string
const header = ref('App lista de compras');
const shoppingIcons =('material-icons shopping-cart-icon')
//creando una referencia reactiva
//para almacenar la lista de compras
const items = ref([
{id: 0, label:'Leche'},
{id: 1, label:'Arroz'},
{id: 2, label:'Carne'},
{id: 3, label:'Pan'},
{id: 4, label:'Huevos'}
]);
const newitem =ref('');
</script>

<template>
  <h1><i v-bind:class="shoppingIcons">local_mall</i>{{header}}</h1>
  <input v-model="newitem" type ="text" placeholder="Agregar articulo">
  <ul>
    <li v-for="{id, label } in items" v-bind:key="id"> ⭐{{ i }} {{ label }}</li>
   
  </ul>
</template>
 
<style scoped>
.shopping-cart-icon{
  font-size:  2rem;
}
</style> 

