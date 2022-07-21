<template>
 <span>
 <slot v-bind:user="user">

 </slot>
 </span>
</template>
<script setup>
import {ref} from 'vue';
const user=ref("beratt")

</script>
