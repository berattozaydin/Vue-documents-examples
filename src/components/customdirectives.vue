<script setup>
const vFocus={mounted:(el)=>el.focus() 
}
function show(){
    alert();
}
const user = "berat";
//v kodları içeriklere müdahale etmeye yarıyor mesela v-focus ile yazarsak sayfaya ilk girildiğinde textbox ta focus lanıyor.
</script>

<template>
<component></component>
    <div>
        <input v-focus />
        <button v-on:click="show">Tıkla</button>
        <h1 v-text="user"></h1>
    </div>
</template>