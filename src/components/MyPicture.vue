<template>
    <div>
       <img :src="avatar" :alt="descricao">
    </div>
</template>

<script>
    export default {
        name: 'MyPicture',
        data() {
            return {
               avatar: "/img/avatar.png",
               descricao: 'Fabricio marques'
            }
        },
    }
</script>