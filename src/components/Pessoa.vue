<template>
    <div>
        <h2> Esta é a descrição da pessoa: {{ name }} </h2>
        <Info :email="email" :esta_trabalhando=false />
        <Form/>

    </div>

</template>
<script>
    import Info from './Info'
    import Form from './Form'

    export default {
        name: 'Pessoa',
        components: {
            Info,
            Form
        },
        data() {
            return {
             name:'Matheus',
             email: 'wendy.t.n5@hotmail.com'

            }
        }
    }
</script>