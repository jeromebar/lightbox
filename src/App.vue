<template>
  <div id="app">
    <div>
      <a :href="`http://lorempicsum.com/futurama/800/600/${n}`" v-lightbox v-for="n in 9" :key="n + '-' + 'picture'">
        <img :src="`http://lorempicsum.com/futurama/150/150/${n}`">
      </a>

        <a :href="`http://lorempicsum.com/rio/800/600/${n}`" v-lightbox="'rio'" v-for="n in 9" :key="n + '-' + 'picture'">
          <img :src="`http://lorempicsum.com/rio/150/150/${n}`">
        </a>
      </div>
    <lightbox></lightbox>
  </div>
</template>

<script>
import Lightbox from './components/lightbox/Lightbox'
export default {
  data () {
    return {
      title: 'futurama'
    }
  },
  components: {
    Lightbox
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
