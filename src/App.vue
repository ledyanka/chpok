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
    import searchCup from 'searchCup.vue';

    const debounce = function (f, ms) {
        let timer = null;
        return function (...args) {
            const onComplete = () => {
                f.apply(this, args);
                timer = null;
            }
            if (timer) {
                clearTimeout(timer);
            }
            timer = setTimeout(onComplete, ms);
        };
    }

    export default {
        data: function () {
            return {
                keywords: '',
                searchArr: []
            }
        },
        watch: {
            keywords(after, before) {
                this.FetchData();
            }
        },
        methods: {
            FetchData: debounce(function () {
                if(!this.keywords) return this.searchArr = []
                axios.get('/api/search', {
                        params: {
                            keywords: this.keywords
                        }
                    })
                    .then(res => {
                        this.searchArr = res.data
                    })
                    .catch(err => {

                    });
            }, 200)
        }
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
