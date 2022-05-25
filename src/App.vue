<template>
  <div id="mm">   
    <h3>{{ sitename }}</h3>
    <HelloWorld msg="Welcome, dude!" />
    <TabsSample :items="this.items" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TabsSample from './components/TabsSample.vue'

export default {
  name: 'App',
  components: { HelloWorld, TabsSample },

  data() {
    return {
      sitename: "Hello, honey!",
      items: [
        { tab: "Pink", content: ["pink"] },
        { tab: "Blue", content: ["blue"] },
        { tab: "Yellow", content: ["yellow"] },
      ]
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