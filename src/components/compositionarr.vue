<script setup>
import composition from "./composition.vue";
 import {ref,defineProps,defineEmits} from 'vue';
const phone1=ref();
const phone2 = ref();
function show(phone11,phone22){
    phone1.value=phone11.value;
    phone2.value=phone22.value;
}

</script>
<template>
 
 <div class="container">
 <div class="row">
 <div class="col-12">
 <h1>{{phone1}}</h1>
 <h1>{{phone2}}</h1>
 <composition @on-compare="show"/>
 </div>
 </div>
 </div>
</template>
