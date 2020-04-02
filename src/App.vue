<template>
  <div id="app">
    <app-nav-bar></app-nav-bar>
    
    <app-banner></app-banner>
    <app-About></app-About>
    <!-- <app-qualities></app-qualities> -->
    <app-Resume></app-Resume>
    <app-projects></app-projects>
    <app-social></app-social>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Banner from './components/Banner.vue'
import Qualities from './components/Qualities.vue'
import Resume from './components/Resume.vue'
import Projects from './components/Projects.vue'
import Social from './components/Social.vue'
import Footer from './components/Footer.vue'
import NavBar from './components/NavBar.vue'
import About from './components/About.vue'

export default {
  name: 'App',
  components: {
    appBanner: Banner,
    appAbout: About,
    appQualities: Qualities,
    appResume: Resume,
    appProjects: Projects,
    appSocial: Social,
    appFooter: Footer,
    appNavBar: NavBar
  }
}
</script>

<style lang="scss">
  @import './styles/custom_bootstrap.scss';
  @import '../node_modules/bootstrap/scss/bootstrap.scss';
</style>

<style>
body {
  margin-top: 60px;
}
h1, h2, h3, h4, h5 {
  font-family: 'Roboto Condensed', sans-serif;
}

.height-100 {
  min-height: 100vh;
}
.height-80 {
  min-height: 80vh;
}
.height-60 {
  min-height: 60vh;
}
.height-50 {
  min-height: 50vh;
}
.height-40 {
  min-height: 40vh;
}


#banner {
  background: url('https://cdn.pixabay.com/photo/2017/08/07/09/00/theatre-2601686_1280.jpg');
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}

#about,
#projects{
  background-color:#F2F2F2;
}

</style>