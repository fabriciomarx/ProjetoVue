<template>
    <div>
        <form action="">
            <InputText/>
            <InputText/>
            <SubmitForm/>
        </form>
    </div>
</template>

<script>
    import InputText from './form/InputText.vue'
    import SubmitForm from './form/SubmitForm.vue'

    export default {
        name: 'MyForm',
        components: {
            InputText,
            SubmitForm
        }
    }
</script>