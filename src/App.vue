<template>
  <div id="app" >
    <nav class="animated fadeIn">
      <div class="nav-item" v-bind:class="{active: ParticlesShow}" @click="ParticlesShow = true,confessionShow = true,todoShow = true,resumeShow = true,musicShow = true,clockShow=true"></div>
      <div class="nav-item" @click="confessionShow = true,ParticlesShow = false,todoShow = true,resumeShow = true,musicShow = true,clockShow=true"></div>
      <div class="nav-item" @click="confessionShow = true,ParticlesShow = false,todoShow = true,resumeShow = false,musicShow = true,clockShow=true"></div>
      <div class="nav-item" @click="confessionShow = true,ParticlesShow = false,todoShow= false,resumeShow = false,musicShow = true,clockShow=true"></div>
      <div class="nav-item" @click="confessionShow = true,ParticlesShow = false,todoShow= false,resumeShow = false,musicShow = false,clockShow=true"></div>
      <div class="nav-item" @click="confessionShow = false,ParticlesShow = false,todoShow= false,resumeShow = false,musicShow = false,clockShow = true"></div>
      <div class="nav-item"></div>
    </nav>

    <transition
      name="custom-classes-transition"
      enter-active-class="animated slideInDown"
      leave-active-class="animated slideOutUp">
      <Particles v-show="ParticlesShow"></Particles>
    </transition>

    <transition
      name="custom-classes-transition"
      enter-active-class="animated slideInDown"
      leave-active-class="animated slideOutUp">
      <Project v-show="resumeShow" v-bind:project="resume"></Project>
    </transition>

    <transition
      name="custom-classes-transition"
      enter-active-class="animated slideInDown"
      leave-active-class="animated slideOutUp">
      <Project v-show="todoShow" v-bind:project="todo"></Project>
    </transition>

    <transition
      name="custom-classes-transition"
      enter-active-class="animated slideInDown"
      leave-active-class="animated slideOutUp">
      <Project v-show="musicShow" v-bind:project="music"></Project>
    </transition>

    <transition
      name="custom-classes-transition"
      enter-active-class="animated slideInDown"
      leave-active-class="animated slideOutUp">
      <Project v-show="confessionShow" v-bind:project="confession"></Project>
    </transition>

    <transition
      name="custom-classes-transition"
      enter-active-class="animated slideInDown"
      leave-active-class="animated slideOutUp">
      <Project v-show="clockShow" v-bind:project="clock"></Project>
    </transition>

    

    

    
    
  </div>
</template>

<script>
import Particles from './components/Particles'
import Project from './components/Project'

export default {
  data(){
    return{
      ParticlesShow:true,
      confessionShow:true,
      todoShow:true,
      resumeShow:true,
      musicShow:true,
      clockShow:true,
      confession:{
        class:'confession',
        name:'天农，表白，墙',
        technologyStack:'Vue ES6 Webpack Less',
        description:'一款基于LeanCloud为后台的表白墙网站，以Vue为框架，可登陆和注册，并提供发帖（图片上传）、评论、点赞等功能。',
        url:'https://hubingliang.github.io/Confession-wall/dist/',
        computer:'../static/computer.png',
        page:'../static/confession.png'
      },
      todo:{
        class:'todo',
        name:'待办事项应用',
        technologyStack:'Vue ES6 Webpack Less',
        description:'基于Vue做的一个待办事项单页应用，原生js生成日历，可对当月事项做一个简单的管理。',
        url:'https://hubingliang.github.io/ToDo/dist/',
        computer:'../static/computer.png',
        page:'../static/todo.png'
      },
      resume:{
        class:'resume',
        name:'在线简历生成器',
        technologyStack:'Vue ES6 Webpack Less',
        description:'在线的简历生成器，提供在线预览功能。',
        url:'https://hubingliang.github.io/vue-resumer/dist/',
        computer:'../static/computer.png',
        page:'../static/resume.png'
      },
      music:{
        class:'music',
        name:'手机端网易云',
        technologyStack:'jQuery less gulp HTML5 CSS3',
        description:'用jQuery写的手机端网易云，主页面、播放页面、热歌榜、搜索页面（可检索）。提供十首歌的播放。',
        url:'https://hubingliang.github.io/NetEase-cloud-music/dist/',
        computer:'../static/iphone.png',
        page:'../static/music.png'
      },
      clock:{
        class:'clock',
        name:'原生JS实现时钟',
        technologyStack:'html css js',
        description:'用原生js实现一个时钟。',
        url:'https://hubingliang.github.io/project/clock/clock.html',
        computer:'../static/computer.png',
        page:'../static/clock.png'
      },
    }
  },
  name: 'app',
  components: {
    Particles,Project
  }
}
</script>

<style>
</style>
