<template>
  <div class="page_banner parallax-window" data-parallax="scroll" :data-image-src="pageBanner"></div>
</template>

<script>
import $ from 'jquery'
import '../../static/parallax.min.js'

export default {
  name: 'Banner',
  props: {
    pageBanner: {
      type: String
    }
  },
  data () {
    return {
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
