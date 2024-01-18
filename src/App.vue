<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  components:{
    AppHeader,
    AppMain,
    AppFooter
  },

  data() {
    return {
      list: [
        {
        name: 'trainings',
        links: [
          'Riding Lesson',
          'Safe Driving',
          'Mountain Bike',
          'Trail Drive',
          'Pedaling'
        ]
      },
      {
        name: 'quicklinks',
        links: [
          'Home',
          'About Us',
          'Blog',
          'Packages',
          'Contact'
        ]
      }
    ],
    }
  },
}
</script>
<template lang="">
  <AppHeader :menu="list[1].links" :trainings="list[0].links"/>
  <AppMain />
  <AppFooter />
</template>
<style lang="scss">
  @use './styles/generals.scss';
</style>