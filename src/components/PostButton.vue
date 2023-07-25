
<template>
    <button class="post-btn">ACCEDER</button>
</template>

<script lang="ts" setup>
</script>

<style scoped> /* scoped se refiere a que estos estilos solo se apliquen a este componente*/
    .post-btn{
        padding: 15px;
        background-color: blueviolet;
        color: white;
        border: 0;
        outline: 0;
    }

    .post-btn:hover { /* hover permite establecer un segundo estado en cualquier elemento */
        background-color: white;
        color: blue;
    }
</style>

