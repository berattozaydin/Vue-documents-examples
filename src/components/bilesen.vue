<template>
    <div id="Bilesen">
    <h1>{{props.title}}</h1>
        <p>{{props.name}}</p>
        <p>{{props.age}}</p>
    </div>
</template>
<script setup>
import {defineProps} from 'vue'
const props = defineProps(['title','name','age'])

</script>