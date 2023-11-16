<template>
  <div>
    <!-- <EventosDom /> -->
    <!-- <FormulariosTeste /> -->
    <!-- <PropriedadeComputada /> -->
    <!-- <ObservadoresVue /> -->
    <!-- <LifeCycle /> -->
    <SlotComponents>
     
      <template v-slot:description>
        <p>dfsdf</p>
      </template>
      Content do header - menu
    </SlotComponents>
  </div>
</template>

<script>
import SlotComponents from './components/SlotComponents.vue'
// import LifeCycle from './components/LifeCycle.vue'
// import ObservadoresVue from './components/ObservadoresVue.vue'
// import PropriedadeComputada from './components/PropriedadeComputada.vue'
// import FormulariosTeste from './components/FormulariosTeste.vue'
// import EventosDom from './components/EventosDom.vue'

export default {
  components: { SlotComponents },
  // components: { LifeCycle },
  // components: { ObservadoresVue },
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
