<template>
  <PrimeiroComponente />
  <LifeCycle />
  <MyPessoa />
</template>

<script>

  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import LifeCycle from './components/LifeCycle.vue'
  import MyPessoa from './components/MyPessoa.vue'

  export default {
    name: 'App',
    components: {
      PrimeiroComponente,
      LifeCycle,
      MyPessoa
    }
  }
</script>