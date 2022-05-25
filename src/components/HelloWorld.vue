<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <textarea v-model='sitename' />
    <button @click='sendTo()' {{ msg }}> </button>

    <p>
      <BigCup :msg='sitename' />
    </p>
  </div>
</template>

<script>
import BigCup from './BigCup.vue'

export default {
    name: 'HelloWorld',
    components: { BigCup },
    props: { msg: String },
    data() {
      return {
        count: 1,
        sitename: "Goose"
      }
  },

}
</script>