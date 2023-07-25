<!--
<template>
    <p v-bind:class="{'danger': hasError,}">El mensaje se a enviado satisfactoriamente.</p>
</template>

<script lang="ts" setup>
    let hasError = true;
</script>
    
<style>
    .danger{
        color: red;
    }
</style>
-->


<!--Otro ejemplo-->

<template>
    <p v-bind:style="{backgroundColor: '#010303', color: c}">El mensaje se a enviado satisfactoriamente.</p>
    <button v-on:click="handleClick">Cambiar color</button>
</template>

<script lang="ts" setup>
    import {ref} from  'vue';
    let c = ref ('#fff');

    const handleClick = () => (c.value = '#03D6C6')
</script>
    
<style>
    
</style>