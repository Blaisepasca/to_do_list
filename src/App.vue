<template>
  <HomeComponents/>
  <InputComponents/>
  <AddtaskComponents/>
  
</template>

<script>

import HomeComponents from './components/HomeComponents.vue'
import InputComponents from './components/InputComponents.vue'
import AddtaskComponents from './components/AddtaskComponents.vue'

export default {
  name: 'App',
  components: {
    HomeComponents,
    InputComponents,
    AddtaskComponents,
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  
  
  
}
</style>
