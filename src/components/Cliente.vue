<template>
    <div :class="{'cliente': !isPremium, 'cliente-premium':isPremium}">

        <h4>Nome: {{cliente.nome}}</h4>
        <hr>
        <p>Email: {{cliente.email}}</p>
       <!-- <p v-if="mostraIdade === true">Idade: {{cliente.idade}}</p>--> <!--If e else direto no html-->
        <!--<p v-else> Esse usuário optou por não exibir sua idade.</p> -->

        <p v-show="mostraIdade === true">idade: {{cliente.idade}}</p>

       <!-- <button @click="">Mudar cor</button>-->

        <!--<input type="text" v-model="nome"> Two way data binding
        <hr>
        <input type="text" :value="descricao"><One way data binding
         <h2 id="cliente-nome">{{nome}}</h2>
    -->
        
    </div>
   
   
</template>

<script>
export default {
    data(){
        return{
          isPremium: false
        }
    },
    props:{ 
       cliente      : Object,
       mostraIdade  : Boolean,
    }
}
</script>

<style scoped>
   .cliente{
       
       background-color: #ECE5E3;
       max-width: 600px;
      
       padding: 1%;
       margin-top:2%
   }

   .cliente-premium{

       background-color: #dfbd00;
       max-width: 600px;
      
       padding: 1%;
       margin-top:2%

   } 
</style>