<template>
    <div>
        <p>Meu nome é: {{nome}}</p>
    </div>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return {
            nome: "Ainda não sei"
        }
    },
    created(){
        setTimeout(() => {
            this.nome = "Fabricio"
        }, 1000);
    },
    mounted(){
        setTimeout(() => {
            this.nome = 'Pedro'
        }, 2000);
    }
}
</script>