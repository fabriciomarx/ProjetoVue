<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento </p>
        <p v-else>Utilizo as seguintes tecnologias</p>
        <ul>
            <li>JS</li>
            <li>PHP</li>
            <li>PYTHON</li>
        </ul>

        <p v-show="mostrar_email">Mande uma mensagem para: {{email}}</p>
    </div>
</template>

<script>
    export default {
        name: 'MyInfo',
        data() {
            return {
                esta_trabalhando: false,
                mostrar_email: true,
                email: 'fabricio_m.s@hotmail.com'
            }
        },
    }
</script>