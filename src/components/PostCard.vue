<template>
    <div class="post-card">
        <h3>Título</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo magnam et ipsum laudantium! Eos placeat laborum inventore, neque possimus asperiores itaque dolores unde necessitatibus, reiciendis nostrum molestiae, dicta quis eaque!</p>
        <PostButton/>
    </div>
</template>

<script lang="ts" setup>
    import PostButton from './PostButton.vue'
</script>

<style scoped>
    .post-card{
        border-radius: 15px;
        padding: 10px;
        margin: 5px;
        border: 1px solid #eee;
    }
</style>