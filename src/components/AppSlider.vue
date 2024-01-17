<script>
export default {
    data() {
        return {
            autoscroll: null,
            currentImg: 0,
            listImg:[
                {
                    name: 'Professional Cycling Club',
                    img: '../assets/slider-bike-4.jpg'
                },
                {
                    name: 'Unforgettable Cycling Experience',
                    img: '../assets/slider-bike-9.jpg'
                },
                {
                    name: 'Learn Mountain Bike From The Expert',
                    img: '../assets/slider-bike-12.jpg'
                }
            ]
        }
    },
    created() {
        this.setAutoscroll()
    },
    methods: {
        nextImg(){
            if (this.currentImg == this.listImg.length - 1) {
                this.currentImg = 0;
            }else{
                this.currentImg++;
            }
        },
        prevImg(){
            if (this.currentImg == 0) {
                this.currentImg = this.listImg.length - 1;
            }else{
                this.currentImg++;
            }
        },
        setAutoscroll(){
            this.autoscroll = setInterval(()=>{
                this.nextImg();
            }, 8000)
        }
    },
}
</script>
<template lang="">
    <div class="">
        <img :src="listImg[currentImg].img" :alt="listImg[currentImg].name">
        <div class="">
            <h1>{{ listImg[currentImg].name }}</h1>
            <span>Learn cycling from the pros.</span>
            <button>Learn More -></button>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partial/variables';
    @use '../styles/generals.scss';
</style>