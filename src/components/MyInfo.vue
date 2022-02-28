<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento </p>
        <p v-else>Utilizo as seguintes tecnologias</p>
        <ul>
            <li>JS</li>
            <li>PHP</li>
            <li>PYTHON</li>
        </ul>

        <p v-show="mostrar_email">Mande uma menssssagem para: {{email}}</p>
        <p>Para acessar meu portifólio <a v-bind:href="meu_link">basta clicar aqui</a></p>

        <MyPicture />
    </div>
</template>

<script>
    import MyPicture from './MyPicture.vue'

    export default {
        name: 'MyInfo',
        components: {
            MyPicture
        },
        data() {
            return {
                esta_trabalhando: true,
                mostrar_email: true,
                email: 'fabricio_m.s@hotmail.com',
                meu_link: 'htpps://google.com.br'
            }
        },
    }
</script>