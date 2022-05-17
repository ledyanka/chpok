<template>
  <div id="mm">   
    <h3>{{ sitename }}</h3>
    <HelloWorld msg="Welcome!" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: { HelloWorld },

  data() {
    return {
      sitename: "Hello, honey!"
    }
  },
}
</script>


<style>
#mm {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #1b8af8;
  margin-top: 60px;
}
</style>
