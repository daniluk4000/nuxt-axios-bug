<template>
  <div class="container">
    <div
      @click="testLoadingFalse" class="button button--green"
    >
      Click here to test request with loading: false option
    </div>
    <div
      @click="testLoadingUnset" class="button button--grey"
    >
      Click here to test request without loading: false option
    </div>
    <div>
      First one should do request <a target="_blank" href="https://axios.nuxtjs.org/options#progress">without</a> loading progress. But
      it shows up.
    </div>
  </div>
</template>

<script>
    import Logo from '~/components/Logo.vue'

    export default {
        components: {
            Logo
        },
        methods: {
            testLoadingFalse() {
                this.$axios.$get('/sample', {
                    progress: false
                })
            },
            testLoadingUnset() {
                this.$axios.$get('/sample')
            },
        }
    }
</script>

<style>
  .container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .title {
    font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
  }

  .subtitle {
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
    padding-bottom: 15px;
  }

  .links {
    padding-top: 15px;
  }

  .container {
    display: flex;
    flex-direction: column;
  }

  .container .button {
    margin: 0 0 10px;
  }
</style>
