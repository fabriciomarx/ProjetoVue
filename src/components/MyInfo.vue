<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento </p>
        <p v-else>Utilizo as seguintes tecnologias</p>
        <ul>
            <li v-for="(item,index) in backend_tecnologias" :key="index">{{item}}</li>
        </ul>
        <p>----------</p>
        <ul>
            <li v-for="item in frontend_tecnologias" :key="item.id">{{item.linguagem}}</li>
        </ul>

        <p v-show="mostrar_email">Mande uma menssssagem para: {{email}}</p>
        <p>Para acessar meu portifólio <a v-bind:href="meu_link">basta clicar aqui</a></p>

        <div><button @click="mostrarEmail"> {{textoBotao}} </button></div>
        <div><ButtonForm @click="mostrarEmail"/></div>
        <div><MyPicture /></div>
    </div>
</template>

<script>
    import MyPicture from './MyPicture.vue'
    import ButtonForm from './form/ButtonForm.vue'

    export default {
        name: 'MyInfo',
        components: {
            MyPicture,
            ButtonForm
        },
        data() {
            return {
                esta_trabalhando: true,
                mostrar_email: false,
                email: 'fabricio_m.s@hotmail.com',
                meu_link: 'https://google.com.br',
                textoBotao: 'Mostrar email',
                backend_tecnologias: ['JS','PHP','PYTHON'],
                frontend_tecnologias: [
                    {id: 1, linguagem: 'JS'},
                    {id: 2, linguagem: 'PHP'},
                    {id: 3, linguagem: 'PYTHON'}
                ]
            }
        },
        methods: {
            mostrarEmail() {
                this.mostrar_email = !this.mostrar_email

                if(!this.mostrar_email) {
                    this.textoBotao = 'Mostrar e-mail'
                }else {
                    this.textoBotao = 'Esconder e-mail'
                }
            }
        }
    }
</script>