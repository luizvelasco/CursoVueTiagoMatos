<template>
    <div>
        <TheHeader />
        <h1>Hello World</h1>
        {{ name }}
    </div>
</template>

<script>
import TheHeader from './TheHeader.vue';
export default {
  components: { TheHeader },
    name: 'LifeCycle',
    data() {
        return {
            name: 'Jon Snow'
        }
    },
    // Criação
        // Preparar o componente
        // Ajax, inicializar algumas variáveis
        // Não tem acesso ao tempolate (DOM)
    // Montagem
        // Inicializar uma lib externa (new lib())
        // precisa de acesso ao template (DOM)
        // Tem acesso ao template (DOM)
    // Atualização
        // Debug
        // Update
    // Desmontagem
        // Remover tudo o que for necessário para liberar memória (lib->destroy)
    // Hooks
    beforeCreate(){
        console.log('before create');
        console.log('Estado', this.name);
        console.log('DOM', this.$el);
    },
    created(){
        console.log('created');
        console.log('Estado', this.name);
        console.log('DOM', this.$el);
    },
    beforeMount(){
        console.log('beforeMount');
        console.log('Estado', this.name);
        console.log('DOM', this.$el);
    },
    mounted(){
        console.log('mounted');
        console.log('Estado', this.name);
        console.log('DOM', this.$el);
    },
    beforeUnmount(){
        console.log('beforeUnmount');
    },
    unmounted(){
        console.log('unmounted');
    }
}
</script>