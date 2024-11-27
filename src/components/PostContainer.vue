<template>
    <h1>Container</h1>
    <div class="post-container">
        <PostCard />
        <PostCard />
        <PostCard />
        <PostCard />
    </div>
</template>

<script setup>
import PostCard from './PostCard.vue';
</script>

<style scoped>
    h1 {
        text-align: center;
    }

    .post-container{
        margin: auto;
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 20px;
        padding: 20px;
    }
</style>