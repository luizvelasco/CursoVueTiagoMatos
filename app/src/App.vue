<template>
  <div>
    <EventosDom />
    <!-- <FormulariosTeste /> -->
  </div>
</template>

<script>
// import FormulariosTeste from './components/FormulariosTeste.vue'
import EventosDom from './components/EventosDom.vue'

export default {
  // components: { FormulariosTeste },
   components: { EventosDom }
  
  
}
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
