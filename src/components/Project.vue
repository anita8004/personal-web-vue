<template>
  <main id="main">
    <div class="page_banner parallax-window" data-parallax="scroll" :data-image-src="banner">
    </div>
    <section class="page_wrap" id="project">
      <div class="container">
        <h2 class="page_title wow fadeInDown">PROJECT</h2>
        <div class="page_content">
          <ul class="project_list" id="projectList">
            <li class="wow flipInY" v-for="project in projects" :key="project.id">
              <a :href="project.url" target="_blank">
                <figure>
                  <span class="cover">{{ project.title }}</span>
                  <img :src="project.pic" :alt="project.title">
                </figure>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
  export default {
    name: 'Project',
    data() {
      return {
        banner: require('../assets/images/banner_project.jpg'),
        projects: [{
            id: 1,
            pic: require('../assets/images/project/project1.jpg'),
            title: '旅樂客',
            url: 'http://www.relaxed.com.tw/'
          },
          {
            id: 2,
            pic: require('../assets/images/project/project2.jpg'),
            title: '美無極',
            url: 'http://www.timelessbeauty.com.tw/'
          },
          {
            id: 3,
            pic: require('../assets/images/project/project3.jpg'),
            title: '人之初',
            url: 'http://www.gemcare.com.tw/'
          },
          {
            id: 4,
            pic: require('../assets/images/project/project4.jpg'),
            title: '領航者',
            url: 'http://www.asaiilerfan.com.tw/'
          },
          {
            id: 5,
            pic: require('../assets/images/project/project5.jpg'),
            title: '高創',
            url: 'http://www.gotrend.com.tw/'
          },
          {
            id: 6,
            pic: require('../assets/images/project/project6.jpg'),
            title: '金龍俊',
            url: ''
          },
          {
            id: 7,
            pic: require('../assets/images/project/project7.jpg'),
            title: '八方雲集',
            url: 'http://tw.8way.com.tw/'
          },
          {
            id: 8,
            pic: require('../assets/images/project/project8.jpg'),
            title: '采妍',
            url: 'http://www.tcygroup.com/'
          },
          {
            id: 9,
            pic: require('../assets/images/project/project9.jpg'),
            title: '正隆',
            url: 'http://118.163.57.23/'
          },
          {
            id: 10,
            pic: require('../assets/images/project/project10.jpg'),
            title: '樂酷馬',
            url: 'https://www.lekumabike.com/'
          },
          {
            id: 11,
            pic: require('../assets/images/project/project11.jpg'),
            title: '生華',
            url: 'http://www.senhwabiosciences.com/tw/'
          },
          {
            id: 12,
            pic: require('../assets/images/project/project12.jpg'),
            title: '金典酒店',
            url: 'http://www.splendor-taichung.com.tw/index.php'
          },
          {
            id: 13,
            pic: require('../assets/images/project/project13.jpg'),
            title: '暐康',
            url: 'http://www.wellcare-global.com'
          }
        ]
      }
    }
  }
</script>
