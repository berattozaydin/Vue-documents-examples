<script setup>
    import {ref,defineProps,defineEmits} from 'vue';
    const phone1 = ref();
    const phone2 = ref();
    const props = defineProps(['composition']);
    const emit = defineEmits(['onCompare']);
    function compare(){
        emit("onCompare",phone1,phone2);
    }
</script>

<template>
    <div>
    <input v-model="phone1" placeholder="Telefon Modeli Giriniz"/>
    <input v-model="phone2" placeholder="Telefon Modeli Giriniz"/>
        <button @click="compare"> Karşılaştır </button>
    </div>
</template>