<script setup>
import {ref} from 'vue';
import {defineProps,defineEmits} from 'vue'
const props = defineProps(['table']);
const emit = defineEmits(['onAdd'])
const id = ref(0)
const material = ref(null)
const price =ref(null)
const whomever =ref(null)
function add(){
    emit('onAdd',props.table.id)
}
</script>
<template>
    <div>
        <input v-model="materiall">
        <input v-model="pricee">
        <input v-model="whomeverr">
        <button class="btn btn-success" @click="add()">Add Material</button>
    </div>
</template>