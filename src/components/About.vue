<template>
  <main id="main">
    <div class="page_banner parallax-window" data-parallax="scroll" :data-image-src="banner">
    </div>
    <section class="page_wrap" id="about">
      <div class="container">
        <div class="page_content">
          <article>
            <h3 class="page_title wow fadeInDown">EXPERIENCE</h3>
            <ul class="list list_sty1">
              <li class="wow fadeInLeft" data-wow-delay=".3s">
                <div class="big_tit">U</div>
                <div class="tit">University</div>
                <p class="des">就讀高雄大學</p>
              </li>
              <li class="wow fadeInLeft">
                <div class="big_tit">T</div>
                <div class="tit">Training</div>
                <p class="des">於巨匠接受職前訓練</p>
              </li>
              <li class="wow fadeInRight">
                <div class="big_tit">J</div>
                <div class="tit">Jobs</div>
                <p class="des">在英創達網頁公司擔任網頁切版師</p>
              </li>
              <li class="wow fadeInRight" data-wow-delay=".3s">
                <div class="big_tit">T</div>
                <div class="tit">Training</div>
                <p class="des">參加台北資策會"前端工程師就業養成班"</p>
              </li>
            </ul>
          </article>
          <article class="learning-experience">
            <h3 class="page_title wow fadeInDown">LEARNING EXPERIENCE</h3>
            <section>
              <h4 class="title">大學時期</h4>
              <ul class="learning-list has-img">
                <li class="wow jackInTheBox" v-for="skill in University" :key="skill.id">
                  <img :src="skill.src" :alt="skill.name">
                </li>
              </ul>
            </section>
            <section>
              <h4 class="title">實體課程</h4>
              <p>巨匠、飛肯、資策會</p>
              <ul class="learning-list has-img">
                <li class="wow jackInTheBox" v-for="skill in PhysicalCourse" :key="skill.id">
                  <img :src="skill.src" :alt="skill.name">
                </li>
              </ul>
            </section>
            <section>
              <h4 class="title">線上課程</h4>
              <p>udemy、hahow、youtube直播、六角學院...</p>
              <ul class="learning-list has-img">
                <li class="wow jackInTheBox" v-for="skill in OnlineＣourses" :key="skill.id">
                  <img :src="skill.src" :alt="skill.name">
                </li>
              </ul>
            </section>
            <section>
              <h4 class="title">自我學習</h4>
              <p>利用網路資源和書籍自我學習成長</p>
              <ul class="learning-list has-img">
                <li class="wow jackInTheBox" v-for="skill in SelfStudy" :key="skill.id">
                  <img :src="skill.src" :alt="skill.name">
                </li>
              </ul>
            </section>
            <section>
              <h4 class="title">編輯器</h4>
              <p>學習過程中使用過的各種編輯器</p>
              <ul class="learning-list has-img">
                <li class="wow jackInTheBox" v-for="skill in IDE" :key="skill.id">
                  <img :src="skill.src" :alt="skill.name">
                </li>
              </ul>
            </section>
          </article>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'About',
  data () {
    return {
      banner: require('../assets/images/banner_about.jpg'),
      University: [
        {
          id: 1,
          name: 'Photoshop',
          src: require('../assets/images/logo/Photoshop.png')
        },
        {
          id: 2,
          name: 'illustrator',
          src: require('../assets/images/logo/illustrator.png')
        }
      ],
      PhysicalCourse: [
        {
          id: 1,
          name: 'html5css3',
          src: require('../assets/images/logo/html5css3.png')
        },
        {
          id: 2,
          name: 'sass',
          src: require('../assets/images/logo/sass.png')
        },
        {
          id: 3,
          name: 'jquery',
          src: require('../assets/images/logo/jquery.png')
        },
        {
          id: 4,
          name: 'JavaScript',
          src: require('../assets/images/logo/JavaScript.png')
        },
        {
          id: 5,
          name: 'git',
          src: require('../assets/images/logo/git.png')
        },
        {
          id: 6,
          name: 'nodejs',
          src: require('../assets/images/logo/nodejs.png')
        },
        {
          id: 7,
          name: 'php&mysql',
          src: require('../assets/images/logo/phpmysql.png')
        }
      ],
      OnlineＣourses: [
        {
          id: 1,
          name: 'gulp',
          src: require('../assets/images/logo/gulp.svg')
        },
        {
          id: 2,
          name: 'JavaScript',
          src: require('../assets/images/logo/JavaScript.png')
        }
      ],
      SelfStudy: [
        {
          id: 1,
          name: 'less',
          src: require('../assets/images/logo/less.png')
        },
        {
          id: 2,
          name: 'JavaScript',
          src: require('../assets/images/logo/JavaScript.png')
        },
        {
          id: 3,
          name: 'pug',
          src: require('../assets/images/logo/pug.svg')
        }
      ],
      IDE: [
        {
          id: 1,
          name: 'sublime',
          src: require('../assets/images/logo/sublime.png')
        },
        {
          id: 2,
          name: 'brackets',
          src: require('../assets/images/logo/Brackets.png')
        },
        {
          id: 3,
          name: 'atom',
          src: require('../assets/images/logo/atom.png')
        },
        {
          id: 4,
          name: 'vscode',
          src: require('../assets/images/logo/vscode.png')
        },
        {
          id: 5,
          name: 'webstorm',
          src: require('../assets/images/logo/webstorm.png')
        }
      ]
    }
  }
}
</script>
