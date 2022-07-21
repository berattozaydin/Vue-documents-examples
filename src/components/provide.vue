<script setup>
    import {ref,provide} from 'vue';
import Inject from './inject.vue';
    const number = ref(0);
    function increase(){
        number.value++;
    }
    provide('number',{number,increase});

</script>
<template>
  <div>
  <Inject/>
  </div>
</template>