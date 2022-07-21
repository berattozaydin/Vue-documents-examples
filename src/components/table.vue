<script setup>
import { ref } from "vue";
import TableAdd from "./tableAdd.vue";
import item from './item.vue'
let id = 0;
const material = ref("berat");
const price = ref("berat");
const whomever = ref("berat");
const arr = ref([
  {
    id: 0,
    material: 'berat',
    price: 0,
    whomever: 'berat',
  },
]);
function add(){
    id++;
    arr.value.push(
        {
        id,
        material:material.value,
        price:price.value,
        whomever:whomever.value,
        }
        );
}
function deletee(){
    let index = arr.value.findIndex((item) => item.id == id);
    arr.value.splice(index,1);
}
</script>
<template>
  <div class="container">
    <!--<table class="table ">
      <thead class="table thead-dark">
        <tr>
          <th>ID</th>
          <th>Material Name</th>
          <th>Material Price</th>
          <th>Do By Whomever</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>{{id}}</td>
          <td>{{material}}</td>
          <td>{{price}}</td>
          <td>{{whomever}}</td>
          <td><button @click="remove" class="btn btn-danger">Delete This Element</button></td>
        </tr>
      </tbody>
    </table>-->
        <input v-model="material">
        <input v-model="price">
        <input v-model="whomever">
        <button @click="add()" class="btn btn-success">Add Material</button>
      <item
          v-for="item in arr"
          :item="item"
          :key="item.id"
          @on-delete="deletee"
        />
  </div>
    
</template>
