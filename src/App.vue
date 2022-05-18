<template>
  <div id="mm">   
    <h3>{{ sitename }}</h3>
    <HelloWorld msg="Welcome, dude!" />
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
<script>
import tab from './components/tabTwo.vue'

export default {
  name: 'App',
  components: { tab},

  data() {
    return {
      tab: null,
      items: [
        { tab: "One", content: "Tab 1 Content" },
        { tab: "Two", content: "Tab 2 Content" },
        { tab: "Three", content: "Tab 3 Content" },
        { tab: "Four", content: "Tab 4 Content" },
        { tab: "Five", content: "Tab 5 Content" },
      ],
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
