<template>
  <CounterOption />
  <CounterComposition />
</template>

<script setup>
import CounterComposition from './components/CounterComposition.vue';
import CounterOption from './components/CounterOption.vue';
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
