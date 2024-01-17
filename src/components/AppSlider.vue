<script>
export default {
    data() {
        return {
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
    methods: {
        nextImg(){
            if (this.currentImg == listImg.length - 1) {
                this.currentImg = 0;
            }else{
                this.currentImg++;
            }
        },
        prevImg(){
            if (this.currentImg == 0) {
                this.currentImg = listImg.length - 1;
            }else{
                this.currentImg++;
            }
        }
    },
}
</script>
<template lang="">
    <div class="">
        <img src="" alt="">
        <div class="">
            <h1></h1>
            <span>Learn cycling from the pros.</span>
            <button>Learn More -></button>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partial/variables';
    @use '../styles/generals.scss';
</style>