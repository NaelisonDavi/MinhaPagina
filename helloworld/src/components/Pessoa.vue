<template>
    <div>
        <h2> Meu nome completo é: {{nome}} </h2>
        <Info/>
    </div>
</template>
<script>
    import Info from './Info'
    
    export default {
        name: 'Pessoa',
        components: {
            Info
        },
        data() {
            return {
                nome: 'Naelison Davi Cirilo Oliveira'
            }
            
        }
    }
</script>
