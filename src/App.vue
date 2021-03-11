<template>
  <div id="app" class="w-1/2 mx-auto">
    <h1 class="text-3xl text-left pb-2">Rangordna genom slider</h1>
    <SliderRanking class="mb-20"/>
    <h1 class="text-3xl text-left pb-2">Rangordna genom dra och släpp</h1>
    <DragRanking class="mb-20"/>
  </div>
</template>

<script>
import SliderRanking from './components/SliderRanking.vue'
import DragRanking from './components/DragRanking.vue'

export default {
  name: 'App',
  components: {
    SliderRanking,
    DragRanking
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
