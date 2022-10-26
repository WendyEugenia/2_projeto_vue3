<template>
    <h1>Meu nome é: {{ nome }} </h1>
</template>

<script>
 export default {
    nome: 'lyCycle',
    data() {
        return {
            nome: 'Ainda não sei'
        }
    },
    created() {
        setTimeout(() =>{
            this.nome = 'Wendy'
        }, 1000);
        this.LifeCycle()
    },
    mounted(){
        setTimeout(() =>{
            this.nome = 'Eugenia'
        }, 3000);
        this.LifeCycle()
    },
    methods: {
        LifeCycle() {
        console.log ("Executou");
        }
    }
} 

</script>