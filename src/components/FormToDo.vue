<template>
    <div class="Form-group">
        <p>
            <input v-model="autor" type="text" placeholder="Autor" class="form-control">
        </p>

        <p>
            <input v-model="titulo" type="text" placeholder="Título" >
        </p>
    
        <p>
            <input v-model="paginas" type="text" placeholder="Páginas" class="form-control">
        </p>
        
        <button v-on:click="addCadastro" class="btn btn-primary">Cadastrar</button>
        
    </div>

</template>

<script>
export default {
    name: "FormToDo",
    data(){
        return{
            autor: "",
            
            titulo: "",
            
            paginas: ""
        }
    },
    methods :{  
        addCadastro(){
            this.$emit("emit-cadastro", {autor: this.autor, titulo: this.titulo, paginas: this.paginas});

            this.autor="";
            this.titulo="";
            this.paginas="";
            
        }

    } 
}
</script>