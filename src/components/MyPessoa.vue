<template>
    <div>
        <h2>Descrição pessoa: {{nome}}</h2>
        <MyInfo/>
        <MyForm/>
    </div>
</template>

<script>
import MyInfo from './MyInfo.vue'
import MyForm from './MyForm.vue'
export default {
    name: 'MyPessoa',
    components: {
        MyInfo,
        MyForm
    },
    data() {
        return {
            nome: "Fabricio"
        }
    }
}
</script>