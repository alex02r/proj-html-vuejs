<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },

  data() {
    return {
      list: [
        {
          name: 'Trainings',
          links: [
            'Riding Lesson',
            'Safe Driving',
            'Mountain Bike',
            'Trail Drive',
            'Pedaling'
          ]
        },
        {
          name: 'Quick Links',
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
  <AppFooter :array_list="list"/>
</template>
<style lang="scss">
@use './styles/generals.scss';
</style>