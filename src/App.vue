<template>
  <div id="app">
    <Conversor/>
    <Respuestas/>
  </div>
</template>

<script>
import Conversor from './components/Conversor.vue'
import Respuestas from './components/Respuestas.vue'

export default {
  name: 'App',
  components: {
    Conversor,
    Respuestas
  }
}
</script>

<style>

</style>
