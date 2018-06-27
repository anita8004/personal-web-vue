<template>
  <footer>
    <div class="container">
      <a href="javascript:;" class="scrollTop" v-on:click.prevent="scrollTop"><span class="icon-keyboard_arrow_up"></span></a>
      <p class="copyright">
        copyright by Anita
      </p>
    </div>
  </footer>
</template>

<script>
import $ from 'jquery'
import '../../static/jquery.easing.1.3.js'

export default {
  name: 'Footer',
  methods: {
    scrollTop () {
      $('html,body').animate({
        scrollTop: 0
      }, 800, 'easeInOutSine')
    }
  },
  mounted () {
    $(window).on('scroll resize', function () {
      let scrollTop = $(this).scrollTop()
      let height = $(this).height()
      if (scrollTop < height) {
        $('.scrollTop').removeClass('fadeIn')
      } else {
        $('.scrollTop').addClass('fadeIn')
      }
    }).trigger('scroll resize')
  }
}
</script>
