<template>
    <div>
        <p v-if="esta_trabalhando">Atualmente estou trabalhando em um projeto.</p>
        <p v-else>Estou disponível para novas oportundades!</p>
        <p> Utilizo as seguintes tecnologias para back-end:</p>
        <ul>
            <li v-for="(technology, index) in tecnologias_backend" v-bind:key="index">
                {{technology}}
            </li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end:</p>
        <ul>
            <li v-for="technology in tecnologias_frontend" :key="technology.id">
                {{technology.language}}
            </li>
        </ul>
        <div>
            <button @click="showEmail">{{textoBotao}}</button>
        </div>
        <p v-show="mostrar_email">Meu e-mail: {{email_link}}</p>
        <p> Meu perfil no github: <a v-bind:href="github_link" target="_blank">clique aqui</a></p>
    </div>
</template>
<script>
export default {
    name: 'Info',
    data(){
        return{
            esta_trabalhando: true,
            mostrar_email: false,
            email_link: 'n.davi.c.oliveira@gmail.com',
            github_link: 'https://github.com/NaelisonDavi',
            textoBotao: 'Mostrar e-mail',
            tecnologias_backend: ['Python','JavaScript','PHP'],
            tecnologias_frontend: [
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'Vue'}
            ]
        }
    },
    methods: {
        showEmail() {
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email) {
                this.textoBotao = 'Mostrar e-mail'
            } else {
                this.textoBotao = 'Esconder e-mail'
            }
        }
    }
}
</script>
