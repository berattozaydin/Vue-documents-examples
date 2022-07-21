<script setup>
import { ref } from "vue";
import item from "./item.vue";
import loginPage from "./loginPage.vue";
let id = 0;
const isShow = ref(false);
const name =ref();
function show() {
  isShow.value = !isShow.value;
}
const msg = ref("berat");
const description = ref("berat");
const doing = ref("berat");
const arr = ref([
  {
    id: 0,
    name: "berat",
    doing:' ',
    description:' ',
    
  },
]);
function add() {
  id++;
  arr.value.push({
    id,
    name: msg.value,
    doing: doing.value,
    description: description.value,
  });
  msg.value = "";
  doing.value="";
  description.value="";

}
function deletee(id) {
  let index = arr.value.findIndex((item) => item.id == id);
  if (index < 0) {
    alert("Böyle bir id yok");
  } else {
    arr.value.splice(index, 1);
  }
}
function login(userName){
    name.value=userName.value;
}
</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col-12">
      <table class="table table-dark">
      <thead>
        <tr>
        <th>Name</th>
        <th>Doing</th>
        <th>Description</th>      
        </tr>
      </thead>
      <tbody>
      <tr>
       <td> <input v-model="msg" /></td>
       <td><input v-model="doing" /></td> 
        <td><input v-model="description" /></td>       
        </tr>
        </tbody>
        </table>
        <button @click="add()">Add</button>
      </div>
      <div class="my-auto">
        <item
          v-for="item in arr"
          :item="item"
          :key="item.id"
          @on-delete="deletee"
        />
        <h1>{{name}}</h1>
        <loginPage @onLogin="login"  />
      </div>
    </div>
  </div>
</template>
