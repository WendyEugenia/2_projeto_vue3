<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else> Estou em busca de novas oportunidades! </p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>JavaScript</li>
            <li>PHP</li>
             <li>Python</li>
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
    data() {
        return {
            esta_trabalhando: false,
            mostrar_email:false, // esse clica 
            email: 'wendy.t.n@hotmail.com',
            meu_link:'https://google.com',
            textoBotao: 'Mostrar e-mail'
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