<template>
  <div id="app" >
    <nav class="animated fadeInRight">
      <div class="nav-item" @click="particles = false,unparticles = true" ></div>
      <div class="nav-item" @click="particles = true,unparticles = false"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
    </nav>
    <Particles v-bind:class="{move : particles,moveback : unparticles}"></Particles>
    <Confession v-bind:class="{move : confession,moveback : unconfession}"></Confession>
  </div>
</template>

<script>
import Particles from './components/Particles'
import Confession from './components/Confession'

export default {
  data(){
    return{
      particles: false,
      confession: false,
      unparticles: false,
      unconfession: false,
    }
  },
  name: 'app',
  components: {
    Particles,Confession
  }
}
</script>

<style>
</style>
