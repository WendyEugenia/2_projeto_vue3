<template>
    <ul>
        <li> <a href="">Home</a> </li>
        <li> <a href="">Projetos</a> </li>
        <li> <a href="">Contato</a> </li>
        <li v-if="esta_logado"> <a href="#"> </a>Meu perfil</li>
    </ul>

</template>

<script>
export default{
    name:'Header',
    props:["esta_logado"]
}

</script>

<style scoped>
    ul {
        list-style: none;
        display: flex;
        background-color: #111;
    }

    li {
        margin-right: 10px;
    }

    a {
        color: rgb(245, 242, 236);
        text-decoration: none;
        transition: .5s;
    }

    a:hover {
        color: turquoise;
    }

</style>