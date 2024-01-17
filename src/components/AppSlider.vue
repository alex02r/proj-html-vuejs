<script>
export default {
    data() {
        return {
            autoscroll: null,
            currentImg: 0,
            listImg:[
                {
                    name: 'Professional Cycling Club',
                    img: '/src/assets/slider-bike-4.jpg'
                },
                {
                    name: 'Unforgettable Cycling Experience',
                    img: '/src/assets/slider-bike-9.jpg'
                },
                {
                    name: 'Learn Mountain Bike From The Expert',
                    img: '/src/assets/slider-bike-12.jpg'
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
    <div class="slider">
        <img :src="listImg[currentImg].img" :alt="listImg[currentImg].name">
        <div class="info">
            <h1>{{ listImg[currentImg].name }}</h1>
            <h5 class="my-4">Learn cycling from the pros.</h5>
            <button class="my-button">Learn More -></button>
        </div>
        <div class="next" @click="nextImg"></div>
        <div class="prev" @click="prevImg"></div>
    </div>
</template>
<style lang="scss" scoped>
    @use '../styles/partial/variables' as *;
    @use '../styles/generals.scss';
    .slider{
        position: relative;
        .info{
            position: absolute;
            left: 25%;
            top: 35%;
            transform: translate(-35%);
            width: 30%;
            color: $white;
            h1{
                font-size: 60px;
                font-weight: 900;
            }
            .my-button{
                border: none;
                color: $white;
                background-color: $black;
                font-size: 18px;
                font-weight: 600;
                padding: 20px;
            }
        }
        .next, .prev{
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            width: 60px;
            height: 60px;
            background-color: $black;
            color: $white;
        }
        .next{
            right: 10px;
        }
        .prev{
            left: 10px;
        }
    }
</style>