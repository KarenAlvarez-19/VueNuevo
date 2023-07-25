<template>
    <ul>
        <li v-for="country in countries" :key="country.code">{{ country.name }}</li>
    </ul>
</template>

<script lang="ts" setup>
    import { ref } from 'vue'; // Ref hace referencia a TypeScript y ref hace refencia a javaScript
    let countries = ref([
       {
            code:'es',
            name: 'Spain'
       },
       {
            code:'en',
            name: 'UK'
       },
       {
            code:'fr',
            name: 'France'
       },
       {
            code:'pt',
            name: 'Portugal'
       },
    ])

</script>

<style scoped>
</style>