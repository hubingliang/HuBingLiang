<template>
  <div class="confession animated">
      <img src="https://i.loli.net/2017/09/27/59cb2fe65be8f.png" alt="1460387448771.jpg" title="1460387448771.jpg" class="page" v-bind:class="{moveleft:moveleft,moveright:moveright}"/>
      <img src="https://i.loli.net/2017/09/27/59cb2b0f30174.png" alt="gallery_macbook_large.jpg" title="gallery_macbook_large.jpg" class="computer" v-bind:class="{moveleft:moveleft,moveright:moveright}"/>
      <div class="mask">
          <div class="container">
            <h2 class="animated fadeInLeft">天农，表白，墙</h2>
            <p class="frame animated slideInLeft">Vue ES6 Webpack Less</p>
            <p class="description animated slideInLeft">
                一款基于LeanCloud为后台的表白墙网站，以Vue为框架，可登陆和注册，并提供发帖（图片上传）、评论、点赞等功能。
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
    methods:{
      jump:function(){
          window.open("https://hubingliang.github.io/Confession-wall/dist/")
      }
  }
}
</script>
