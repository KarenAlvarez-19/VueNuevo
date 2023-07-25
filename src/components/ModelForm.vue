<template>
    <form>
        <input  type="text" v-model="inputText"> 
        <input type="checkbox" v-model="agree"/>Acepto términos y condiciones
        <select v-model="country">
            <option value="Opciones">Opciones</option>
            <option value="Spain">Spain</option>
            <option value="UK">UK</option>
            <option value="France">France</option>
        </select>
    </form>
    <h1>{{ inputText }}</h1>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
    let inputText = ref ('')
    let agree = ref (false)
    let country = ref ('Opciones')
</script>

<style scoped>
</style>