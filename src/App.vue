<template>
  <div id="app">
    
    <input type="text" v-model="clienteVictor.nome">
   
    <div v-for="cliente in clientes" :key="cliente.id">
      <h4>{{index}}</h4>
      <Cliente :cliente="cliente"/>
      <hr>
      <h4>Edição:</h4>
      <input type="text" v-model="cliente.nome">
      <input type="text" v-model="cliente.email">
    </div>




    <!--<Cliente :cliente="clienteVictor" :mostraIdade="true"/>
    <Cliente :cliente="clienteVictor" :mostraIdade="false"/>
    <Cliente :cliente="clienteVictor" :mostraIdade="true"/>-->


 
  </div>
</template>

<script>
import Cliente from './components/Cliente'
//import Produto from './components/Produto'

export default {
  name: 'App',
  data(){
    return{
      nomeDoVictor: "Victor kk",
      clienteVictor:{
        nome: "Vitin",
        email:"vitin.com",
        idade:99
      },
      clientes:[
        {
          id: 1,
          nome: "Jota Ce",
          email:"jc@email.com",
          idade:99 
        },
        {
          id:2,
          nome: "Fezinho Pataty",
          email:"fezinho@email.com",
          idade:99
        },
        {
          id: 3,
          nome: "Creito",
          email:"creito@email.com",
          idade:99
        }
      ]
    }
  },
  components: {
    Cliente,
  //  Produto
  }
}
</script>

<style>

</style>
