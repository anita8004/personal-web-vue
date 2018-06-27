<template>
  <main id="main">
    <banner :page-banner="banner"></banner>
    <section class="page_wrap" id="work">
      <div class="container">
        <h2 class="page_title wow fadeInDown">WORK</h2>
        <div class="page_content">
          <aside class="works_aside wow fadeInLeft">
            <h3 class="aside_title">分類</h3>
            <ul class="aside_list filters-button-group">
              <li class="filter filtr-button active filtr-active" data-filter="" v-on:click.prevent="categoryHandler('')">All</li>
              <li class="filter filtr-button" data-filter="css" v-on:click.prevent="categoryHandler('css')">css</li>
              <li class="filter filtr-button" data-filter="javascript" v-on:click.prevent="categoryHandler('javascript')">javascript</li>
              <li class="filter filtr-button" data-filter="html" v-on:click.prevent="categoryHandler('html')">html</li>
            </ul>
            <h3 class="aside_title">關鍵字搜尋</h3>
            <form class="search" id="workSearch">
              <input type="text" placeholder="請輸入關鍵字" class="form-field" v-model="searchKey">
            </form>
          </aside>
          <ul class="works_list filtr-container sameSize" id="worksList">
            <li v-for="work in filterItems" :class="work.category + ' item wow flipInY'" :key="work.id">
              <a :href="work.url" target="_blank">
                <h3 class="item_title">{{ work.title }}</h3>
                <p class="categories">{{ work.category }}</p>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import $ from 'jquery'
import Banner from './Banner'

export default {
  name: 'Work',
  data () {
    return {
      banner: require('../assets/images/banner_work.jpg'),
      works: [
        {
          id: 1,
          title: 'Treasure Hunt',
          url: 'https://jsbin.com/lepiled/3/edit?output',
          category: 'javascript'
        },
        {
          id: 2,
          title: '輪播',
          url: 'https://jsfiddle.net/anita8004/925z85j7/',
          category: 'javascript'
        },
        {
          id: 3,
          title: 'Resize 次數控制',
          url: 'https://jsfiddle.net/anita8004/Loymu2jw/',
          category: 'javascript'
        },
        {
          id: 4,
          title: 'slick範例 - filter',
          url: 'https://jsfiddle.net/anita8004/17s7nopx/',
          category: 'javascript html css'
        },
        {
          id: 5,
          title: '取餘數',
          pic: './images/snow-man.jpg',
          url: 'https://jsfiddle.net/anita8004/a9g8gLsL/',
          category: 'javascript'
        },
        {
          id: 6,
          title: '百葉窗展開收闔',
          url: 'https://jsfiddle.net/anita8004/sm7s1szq/',
          category: 'javascript'
        },
        {
          id: 7,
          title: '卷軸客製化',
          url: 'https://jsfiddle.net/anita8004/tj0zv0uc/',
          category: 'css'
        },
        {
          id: 8,
          title: 'when().then()',
          url: 'https://hackmd.io/s/r1fJF2uE-',
          category: 'javascript'
        },
        {
          id: 9,
          title: 'Json & Map',
          url: 'https://hackmd.io/s/BkV8Cb5Eb',
          category: 'javascript'
        },
        {
          id: 10,
          title: 'Pug 寫法整理',
          url: 'https://hackmd.io/s/Hk2Hui1NW',
          category: 'html'
        },
        {
          id: 11,
          title: 'Array',
          url: 'https://hackmd.io/s/BkCV6EFcG',
          category: 'javascript'
        }
      ],
      searchKey: '',
      category: ''
    }
  },
  methods: {
    categoryHandler (category) {
      let vm = $(event.target)
      vm.addClass('active').siblings().removeClass('active')
      this.category = category
    }
  },
  computed: {
    filterItems () {
      let categoryName = this.category
      let inputValue = this.searchKey
      if (categoryName === '' && inputValue === '') {
        return this.works
      } else if (inputValue !== '') {
        return this.works.filter(function (work) {
          return work.title.match(inputValue)
        })
      } else {
        return this.works.filter(function (work) {
          return work.category.match(categoryName)
        })
      }
    }
  },
  components: {
    Banner
  }
}
</script>
