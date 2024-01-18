<script>
import AppCards from './AppCards.vue';
import AppEvents from './AppEvent.vue';
import jumbotron from './jumbotron.vue';
import AppSlider from './AppSlider.vue';
export default {
    components:{
        AppSlider,
        jumbotron,
        AppEvents,
        AppCards
    }
}
</script>
<template lang="">
    <AppSlider/>
    <jumbotron/>
    <AppEvents />
    <AppCards />
</template>
<style lang="">
    
</style>