<template>
  <div>
    <!-- <EventosDom /> -->
    <!-- <FormulariosTeste /> -->
    <!-- <PropriedadeComputada /> -->
    <ObservadoresVue />
  </div>
</template>

<script>
import ObservadoresVue from './components/ObservadoresVue.vue'
// import PropriedadeComputada from './components/PropriedadeComputada.vue'
// import FormulariosTeste from './components/FormulariosTeste.vue'
// import EventosDom from './components/EventosDom.vue'

export default {
  components: { ObservadoresVue },
  // components: { PropriedadeComputada },
  // components: { FormulariosTeste },
  //  components: { EventosDom }
  
  
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
