<template>
  <main id="main">
    <section class="sect_banner parallax-window" data-parallax="scroll" :data-image-src="banner">
      <div class="container">
        <div class="card">
          <div class="pic">
            <img :src="userImg" alt="Cat">
          </div>
          <h3 class="name animated swing">ANITA</h3>
          <p class="job animated swing">Front-end<br>Engineer</p>
          <a href="#!" class="scrollDown"><span class="icon-keyboard_arrow_down"></span></a>
        </div>
      </div>
    </section>
    <section class="sect sect_work">
      <div class="container">
        <h3 class="title">READ MORE</h3>
        <ul class="list list_sty1">
          <li class="wow fadeInLeft" data-wow-delay=".3s">
            <div class="big_tit">A</div>
            <div class="tit">About</div>
            <p class="des">關於我</p>
            <a href="about.html" class="view">Read More<span class="icon-keyboard_arrow_right"></span></a>
          </li>
          <li class="wow fadeInLeft">
            <div class="big_tit">W</div>
            <div class="tit">Work</div>
            <p class="des">js、css 練習項目</p>
            <a href="work.html" class="view">Read More<span class="icon-keyboard_arrow_right"></span></a>
          </li>
          <li class="wow fadeInRight">
            <div class="big_tit">U</div>
            <div class="tit">UI / UX</div>
            <p class="des">UI / UX 練習項目</p>
            <a href="work.html" class="view">Read More<span class="icon-keyboard_arrow_right"></span></a>
          </li>
          <li class="wow fadeInRight" data-wow-delay=".3s">
            <div class="big_tit">P</div>
            <div class="tit">Project</div>
            <p class="des">web 實作專案</p>
            <a href="project.html" class="view">Read More<span class="icon-keyboard_arrow_right"></span></a>
          </li>
        </ul>
      </div>
    </section>
    <section class="sect sect_project">
      <h3 class="title">CURRENT PROJECT</h3>
      <ul class="pro_list">
        <li v-for="project in currentProject" :key="project.id">
          <a :href="project.url" :data-tit="project.title" target="_blank">
              <img :src="project.img" alt="my-gulp-demo">
          </a>
        </li>
      </ul>
    </section>
    <section class="sect sect_contact parallax-window" data-parallax="scroll" :data-image-src="contactBg">
      <div class="container">
        <div class="content">
          <h3 class="title">CONTACT</h3>
          <a href="mailto:anita8004@gmail.com" class="icon wow fadeInUp"><span class="icon-envelope"></span><span class="txt">Mail</span></a>
          <a href="https://jsfiddle.net/user/anita8004/fiddles/" class="icon wow fadeInUp" target="_blank"><span class="icon-jsfiddle"></span><span class="txt">JsFiddle</span></a>
          <a href="https://github.com/anita8004" class="icon wow fadeInUp" target="_blank"><span class="icon-github"></span><span class="txt">Github</span></a>
          <a href="https://www.linkedin.com/in/yunhsiu-li-442228154/" class="icon wow fadeInUp" target="_blank"><span class="icon-linkedin"></span><span class="txt">LinkIn</span></a>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import $ from 'jquery'
import '../../static/parallax.min.js'

export default {
  name: 'Index',
  data () {
    return {
      banner: require('../assets/images/banner.jpg'),
      userImg: require('../assets/images/cat.jpg'),
      currentProject: [
        {
          id: 1,
          title: 'my-gulp-demo',
          url: 'https://github.com/anita8004/my-gulp-demo',
          img: require('../assets/images/current/my-gulp-demo.jpg')
        },
        {
          id: 2,
          title: 'yunhsiu-web (old)',
          url: 'https://github.com/anita8004/yunhsiu-web',
          img: require('../assets/images/current/old-web.png')
        },
        {
          id: 3,
          title: 'personal-web',
          url: 'https://github.com/anita8004/personal-web',
          img: require('../assets/images/current/personal-web.png')
        },
        {
          id: 4,
          title: 'TreasureHunt',
          url: 'https://github.com/anita8004/TreasureHunt',
          img: require('../assets/images/current/TreasureHunt.png')
        }],
      contactBg: require('../assets/images/contact_bg.jpg')
    }
  },
  mounted () {
    $('.parallax-window').each(function () {
      if ($('.parallax-window').length > 0) {
        $(this).parallax()
      }
    })
  },
  destroyed () {
    $('.parallax-mirror').remove()
  }
}
</script>
