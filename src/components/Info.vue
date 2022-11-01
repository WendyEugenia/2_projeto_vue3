<template>
    <div>
        
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else> Estou em busca de novas oportunidades! </p>
        <p>Utilizo as seguintes tecnologias de Back End:</p>
        <ul>
            <li>JavaScript</li>
            <li>PHP</li>
             <li>Python</li>
        </ul>
        <p>Utilizo as seguintes tecnologias de Front End:</p>
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>Vue</li>
        </ul>
        <div>

            <button @click="showEmail" > {{ textoBotao }}</button>
        </div>
       <p v-show="mostrar_email">Mande um mensagem para: {{ email }} </p>
       <p class="teste" > Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">  basta clicar aqui</a> </p>
       <Picture/>

    </div>
</template>
<script>
import Picture from './form/Picture.vue'

export default {
    name:'Info',
    components: {
        Picture
    },
    props:{
      email: String,
      esta_trabalhando: Boolean
    },
    data() {
        return {
            
            mostrar_email:false, // esse clica 
        
            meu_link:'https://google.com',
            textoBotao: 'Mostrar e-mail',
            backed_tecnologies:['JavaScript', 'PHP', "Python"],
            frontend_tecnologies: [
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'Vue'},
            ]
        }
    },
    methods: {
        showEmail() {
            this.mostrar_email = !this.mostrar_email  // ! significa ao contrario e clica aparece email e clica desparece email
            if(!this.mostrar_email) {
                this.textoBotao = 'Mostrar e-mail'
            } else {
                this.textoBotao ='Esconder e-mail'
            }
        }
    }
}

</script>

<style>
    .paragrafo_pai{
        color: red;
    }
</style>