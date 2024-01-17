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
          'ridinglesson',
          'safedriving',
          'mountainbike',
          'traildrive',
          'pedaling'
        ]
      },
      {
        name: 'quicklinks',
        links: [
          'home',
          'aboutus',
          'blog',
          'packages',
          'contact'
        ]
      }
    ],
    }
  },
}
</script>
<template lang="">
  <AppHeader :menu="list[1].links"/>
  <AppMain />
  <AppFooter />
</template>
<style lang="scss">
  @use './styles/generals.scss';
</style>