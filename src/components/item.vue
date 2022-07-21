<template>
    <div id="Bilesen">
    <table class="table">
    <thead class="thead-dark">
      <tr>
        <th>İd</th>
        <th>Name</th>
        <th>Doing</th>
        <th>Description</th> 
      </tr>
    </thead>
    <tbody>
      <tr>
    <td>{{props.item.id}}</td>
    <td>{{props.item.material}}</td>
    <td>{{props.item.price}}</td>
    <td>{{props.item.whomever}}</td>
    <button @click="deletee">SİL</button>
     </tr>
    </tbody>
  </table>
    </div>
</template>
<script setup>

import {defineProps,defineEmits} from 'vue'
import todo from './todo.vue'
const props = defineProps(['item'])
const emit = defineEmits(['onDelete'])
function deletee(){
    emit('onDelete',props.item.id)
}
</script>