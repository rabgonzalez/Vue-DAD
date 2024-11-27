<template>
    <button class="post-button">Click aquí!</button>
</template>

<script setup>
</script>

<style scoped>
    .post-button{
        background-color: rgb(255, 155, 0);
        color: white;
        font-size: 24px;
        border-radius: 5px;
        padding: 10px 20px;
        transition: background-color 0.3s ease-in-out;
    }

    .post-button:hover{
        background-color: rgb(255, 200, 0);
        cursor: pointer;
    }
</style>