<template>
   <h1 v-if="age < 18">Eres menor de edad</h1> <!--En esta directiva se indica que age solo se va a pintar cuando se cumpla la condicion-->
   <h1 v-else>Eres mayor de edad </h1>
</template>

<script lang="ts" setup>
    let age = 10
</script>

<style scoped>
</style>