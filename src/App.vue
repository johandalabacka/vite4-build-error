<template>
  <div>
    <button @click="hello">Hello</button>
  </div>
</template>

<script>
  import api from './api/index.js'

  export default {
    name: 'App',
    methods: {
      hello () {
        console.log('App.hello')
        api.greetings.hello()
      }
    }
  }
</script>
