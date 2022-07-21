<script setup>
import {ref} from 'vue';
import {defineProps,defineEmits} from 'vue'
const props = defineProps(['loginPage']);
const userName = ref();
const password = ref();
const emit = defineEmits(['onLogin'])
function login(){
    emit('onLogin',userName)
}
</script>

<template>
  <div class="container">
    <div class="row bg-primary"></div>
        <input v-model="userName">
        <input v-model="password">
        <button @click="login">Yakala</button>
  </div>
</template>
