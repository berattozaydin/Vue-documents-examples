<script setup>
    import {inject} from 'vue';
    //const {number,increase} = inject('number');
    const i = inject('number');
    
    
</script>
<template>
    <div>
        <button @click="i.increase">{{i.number}}</button>
    </div>
</template>