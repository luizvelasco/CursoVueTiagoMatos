<template>
    <div>
        <button @click.once="onClick">Enviar</button>
    
        <div @mouseover="onMouseOver" @mouseout="onMouseOut">
            mouseover
        </div>

        <form action="http://google.com" @submit.prevent="onSubmit">
            <button type="submit">Enviar</button>
            <input type="text" @keyup.enter="onKeyUp">
        </form>
    </div>
</template>

<script>
export default {
    name: 'EventosDom',
    data(){

    },
    methods: {
        onClick($evt){
            console.log('Teste', $evt);
        },
        onMouseOver($evt) {
            console.log('mouse over', $evt);
        },
        onMouseOut($evt){
            console.log('mouse out', $evt);
        },
        onSubmit($evt){
            console.log('submit', $evt);
        },
        onKeyUp($evt) {
            console.log('onKeyUp', $evt);
        }
    }
}
</script>