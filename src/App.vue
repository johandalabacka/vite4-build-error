<template>
  <div>
    <button @click="hello">Hello</button>
  </div>
</template>

<script>
  import api from './api/index.js'
  import * as greetings from './api/greetings.js'

  export default {
    name: 'App',
    methods: {
      hello () {
        console.log('App.hello')
        api.greetings.hello()
        greetings.hi()
      }
    }
  }
</script>
