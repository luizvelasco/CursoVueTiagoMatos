<template>
    <div>
        <label for="">Nome</label>
    <input v-model="name" type="text" >

    {{name}}
  <br><br>
    <select v-model="sports" name="" id="">
      <option value="">Escolha</option>
      <option value="futebol">Futebol</option>
      <option value="skate">Skate</option>
      <option value="tenis">Tênis</option>
    </select>
    {{sports}}

    <div>
      <label>Newsletter</label>
      <input v-model="newsletter" type="radio" value="sim">Sim
      <input v-model="newsletter" type="radio" value="nao">Não
      {{newsletter}}
    </div>
      <label>Contrato</label>
      <input v-model="contract" type="checkbox" value="sim">Aceita nosso termo...
      {{contract}}
    <div>
      <div>
        <label for="">Cores</label>
        <input v-model="color" type="checkbox" value="azul">Azul
      <input v-model="color" type="checkbox" value="amarelo">Amarelo
      {{color}}
      </div>

    </div>
    </div>
</template>

<script>
export default {
    name: 'FormulariosTeste',
    data (){
    return {
      name: 'Snow',
      sports: 'skate',
      newsletter: '',
      contract: true,
      color: []
  }
  }
}
</script>