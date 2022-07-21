<script>
export default {
    props:{type:String},
    methods:{
        change(){
            this.$emit('change','yeni başlık')
        },
    },
};
</script>
<template>
    <div>
        {{title}}
        <button @click="change">Change</button>    
    </div>
</template>