<template>
  <h1>{{ msg }}</h1>

  <p>
    <a href="https://vitejs.dev/guide/features.html" target="_blank">Vite Documentation</a> |
    <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Documentation</a> |
        <a href="https://www.primefaces.org/primevue" target="_blank">PrimeVue Documentation</a>
  </p>

  <Button @click="state.count++" label="Count"></Button>
  <h6>{{ state.count }}</h6>

  <h1>Overlay position</h1>

  <Dropdown v-model="select" :options="cities" optionLabel="name" optionValue="code" placeholder="Select a City" />

  <p style="color: red">
    Dropdown position not align. When window height less than 800px
  </p>
</template>

<script setup>
import { defineProps, reactive, ref } from 'vue'

defineProps({
  msg: String
})

const state = reactive({ count: 0 })

const select = ref();
const cities = ref([
    {name: 'New York', code: 'NY'},
    {name: 'Rome', code: 'RM'},
    {name: 'London', code: 'LDN'},
    {name: 'Istanbul', code: 'IST'},
    {name: 'Paris', code: 'PRS'}
]);
</script>

<style scoped>
a {
  color: #42b983;
}
</style>