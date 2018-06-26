<template>
  <header id="header">
    <div class="container">
      <h1 class="logo">Personal Web</h1>
      <button class="hamburger"><span class="icon-menu"></span><span class="text-hide">MENU</span></button>
      <nav class="menu">
        <ul>
          <li>
            <router-link exact to="/">HOME</router-link>
          </li>
          <li>
            <router-link to="/about">ABOUT</router-link>
          </li>
          <li>
            <router-link to="/project">PROJECT</router-link>
          </li>
          <li>
            <router-link to="/work">WORK</router-link>
          </li>
          <!-- <li class="active"><a href="./index.html">HOME</a></li>
          <li><a href="about.html">ABOUT</a></li>
          <li><a href="project.html">PROJECT</a></li>
          <li><a href="work.html">WORK</a></li> -->
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
    }
  }
}
</script>
