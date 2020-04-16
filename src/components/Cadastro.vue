<template>
    <div class="container">
    <h1>Cadastro de Livros</h1>
    <hr/>
    <FormToDo v-on:emit-cadastro = "addCadastro" />
    <!-- Formulario -->
      <div v-for="(c, index) in cadastros" :key="index"> 
          <span>Autor: <strong>{{ c.autor }}</strong></span>
          <P>{{ c.titulo }}</P>
          <P>{{ c.paginas }}</P>
          <!-- Listagem de comentarios-->
          <div>
              <a href="#">Excluir</a>
          </div>
      </div>
    </div>
</template>

<script>
import FormToDo from "./FormToDo.vue";
export default {
    name: "Cadastro",
    components:{
        FormToDo

    },
    data(){ //IMPORTANTE: onde define o modelo. Trabalhar com a reatividade.
        return{
            cadastros: []
        }
    },
    methods: {
        addCadastro(descricao){
            this.cadastros.push(descricao);
        }
    }

}
</script>