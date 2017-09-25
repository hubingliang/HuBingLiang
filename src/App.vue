<template>
  <div id="app">
    <nav class="animated fadeInRight">
      <div class="nav-item"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
      <div class="nav-item"></div>
    </nav>
    <Particles></Particles>
  </div>
</template>

<script>
import Particles from './components/Particles'

export default {
  name: 'app',
  components: {
    Particles
  }
}
</script>

<style>
</style>
