<template>
  <div class="confession animated">
      <img src="https://i.loli.net/2017/09/26/59c9a502730d7.jpg" alt="1460387448771.jpg" title="1460387448771.jpg" class="page" v-bind:class="{moveleft:moveleft,moveright:moveright}"/>
      <img src="https://i.loli.net/2017/09/26/59ca1e9f814f6.jpg" alt="gallery_macbook_large.jpg" title="gallery_macbook_large.jpg" class="computer" v-bind:class="{moveleft:moveleft,moveright:moveright}"/>
      <div class="mask">
          <div class="container">
            <h2 class="animated fadeInLeft">天农，表白，墙</h2>
            <p class="frame animated slideInLeft">Vue</p>
            <p class="description animated slideInLeft"></p>
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
    methods:{
      jump:function(){
          window.open("https://hubingliang.github.io/Confession-wall/dist/")
      }
  }
}
</script>
