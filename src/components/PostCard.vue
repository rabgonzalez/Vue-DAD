<template>
    <div class="post-tarjeta">
        <h3>Tarjeta</h3>
        <p>Esta es mi tarjeta</p>
        <PostButton />
    </div>
</template>

<script setup>
import PostButton from './PostButton.vue';
</script>

<style scoped>
    .post-tarjeta{
         width: 200px;
         height: 300px;
         background-color: #f1f1f1;
         border-radius: 10px;
         padding: 10px;
         margin: 10px;
         box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.2);
         display: flex;
         flex-direction: column;
         align-items: center;
         justify-content: center;
    }
</style>
