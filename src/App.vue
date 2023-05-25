<template>
  <div id="app">
    <div v-if="title == 'futurama'">
      <a :href="'https://picsum.photos/830/600?category=futurama/' + n" v-lightbox v-for="n in 9" v-bind:key="n">
      <img :src="'https://picsum.photos/150/150?category=futurama/' + n" alt="">
    </a>
    </div>

      <div v-if="title == 'rio'">
      <a :href="'https://picsum.photos/830/600?category=rio/' + n" v-lightbox v-for="n in 9" v-bind:key="n">
      <img :src="'https://picsum.photos/150/150?category=rio/' + n" alt="">
    </a>
    </div>

    <button @click="title = 'rio'">RIO</button>
    <button @click="title = 'futurama'">Futurama</button>
    <lightbox></lightbox>
  </div>
</template>

<script>
import Lightbox from './components/Lightbox/Lightbox'
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
