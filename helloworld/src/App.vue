<template>
  <div>
    <Header />
    <OlaLeitor />
    <Pessoa />
    <Form />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Form from './components/Form.vue'
import OlaLeitor from './components/OlaLeitor.vue'
import Pessoa from './components/Pessoa.vue'

    export default {
      name: 'App',
      components:{
        Header,
        OlaLeitor,
        Pessoa,
        Form,
      }
    }
</script>

<style>
  body {
    background-color: rgb(240, 240, 240);
    color:rgb(21, 54, 73);
  }

  a {
    color: rgb(0, 89, 255);
  }
</style>