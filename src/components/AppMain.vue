<script>
import AppEvents from './AppEvent.vue';
import jumbotron from './jumbotron.vue';
import AppSlider from './AppSlider.vue';
export default {
    components:{
        AppSlider,
        jumbotron,
        AppEvents
    }
}
</script>
<template lang="">
    <AppSlider/>
    <jumbotron/>
    <AppEvents />
</template>
<style lang="">
    
</style>