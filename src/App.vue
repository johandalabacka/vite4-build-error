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
        api.greetings.hello() // <--- this is removed on build. Using yarn dev works
        greetings.hi() // <--- this is not removed on build
      }
    }
  }
</script>
