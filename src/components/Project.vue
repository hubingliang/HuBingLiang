<template>
  <div v-bind:class="project.class">
      <img v-bind:src="project.computer"  class="computer" v-bind:class="{moveleft:moveleft,moveright:moveright}"/>
      <img v-bind:src="project.page"  class="page" v-bind:class="{moveleft:moveleft,moveright:moveright}"/>
      
      <div class="mask">
          <div class="container">
            <h2 class="animated fadeInLeft">{{project.name}}</h2>
            <p class="frame animated slideInLeft">{{project.technologyStack}}</p>
            <p class="description animated slideInLeft">
                {{project.description}}
            </p>
            <button class="animated slideInLeft" v-on:mouseenter="moveleft = true,moveright = false"  v-on:mouseleave="moveleft = false,moveright = true" @click="jump">VIEW PROJECT</button>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            moveleft: false,
            moveright: false
        }
    },
    props:['project'],
    methods:{
      jump:function(){
          window.open(`${this.project.url}`)
      }
  }
}
</script>
