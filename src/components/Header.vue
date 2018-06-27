<template>
  <header id="header">
    <div class="container">
      <h1 class="logo">Personal Web</h1>
      <button class="hamburger" v-on:click.prevent="menuToggle"><span class="icon-menu"></span><span class="text-hide">MENU</span></button>
      <nav class="menu">
        <ul>
          <li v-on:click="menuHide">
            <router-link exact to="/">HOME</router-link>
          </li>
          <li v-on:click="menuHide">
            <router-link to="/about">ABOUT</router-link>
          </li>
          <li v-on:click="menuHide">
            <router-link to="/project">PROJECT</router-link>
          </li>
          <li v-on:click="menuHide">
            <router-link to="/work">WORK</router-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
import $ from 'jquery'

export default {
  name: 'Header',
  methods: {
    menuToggle () {
      $(event.currentTarget).toggleClass('open')
      let $menu = $('header .menu')
      $menu.toggleClass('open')
      if ($menu.hasClass('open')) {
        $menu.css({
          transform: 'rotateX(0deg)',
          transition: 'transform .5s cubic-bezier(0.445, 0.05, 0.55, 0.95)'
        })
      } else {
        $menu.css({
          transform: 'rotateX(90deg)',
          transition: 'transform .5s cubic-bezier(0.445, 0.05, 0.55, 0.95)'
        })
      }
    },
    menuHide () {
      let $menu = $('header .menu')
      if ($menu.hasClass('open')) {
        $menu.css({
          transform: 'rotateX(0deg)',
          transition: 'transform .5s cubic-bezier(0.445, 0.05, 0.55, 0.95)'
        })
      }
    }
  },
  mounted () {
    $(window).on('resize', function () {
      let $menu = $('header .menu')
      if (window.matchMedia('(min-width: 769px)')) {
        $('.hamburger').removeClass('open')
        $menu.removeClass('open')
        $menu.css({ transform: '', transition: '' })
      }
    }).trigger('resize')
  }
}
</script>
