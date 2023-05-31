<template>
  <div>
  <h1>Olá leitor!</h1>
  <Picture/>
  <p> meu nome é {{nome}}, sou {{profissao}}</p>
  </div>
</template>

<script>
import Picture from './Picture.vue'
    export default {
      name: 'OlaLeitor',
      components: {
        Picture
      },
      data(){
        return {
            nome: "Davi",
            profissao: "desenvolvedor trainee"
        }
      }
      }
</script>
