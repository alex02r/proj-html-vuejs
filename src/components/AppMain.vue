<script>
import ProfessionalCyclingCard from './ProfessionalCyclingCard.vue';
import AppCards from './AppCards.vue';
import AppEvents from './AppEvent.vue';
import jumbotron from './jumbotron.vue';
import AppSlider from './AppSlider.vue';
export default {
    components:{
        AppSlider,
        jumbotron,
        AppEvents,
        AppCards,
        ProfessionalCyclingCard
    }
}
</script>

<template lang="">
    <AppSlider/>
    <jumbotron/>
    <AppEvents />
    <AppCards />
    <ProfessionalCyclingCard/>
</template>

<style lang="">
    
</style>