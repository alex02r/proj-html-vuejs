<script>
export default {
    data() {
        return {
            proCycling: [
                {
                    image: '/src/assets/training-box-1.jpg',
                    title: 'Riding Lesson',
                }, {
                    image: '/src/assets/training-box-2.jpg',
                    title: 'Safe Driving',
                }, {
                    image: '/src/assets/training-box-3.jpg',
                    title: 'Mountain Bike',
                }, {
                    image: '/src/assets/training-box-4.jpg',
                    title: 'Trail Drive',
                }, {
                    image: '/src/assets/training-box-5.jpg',
                    title: "Pedaling",
                }
            ]
        }
    },
    methods: {
        next() {
            const containerCard = this.$el.querySelector('.container-card');
            containerCard.scrollLeft -= 100;
            this.proCycling.push(this.proCycling.shift())
        },
        previus() {
            const containerCard = this.$el.querySelector('.container-card');
            containerCard.scrollLeft += 50;
            this.proCycling.push(this.proCycling.unshift(this.proCycling[4]));
        },
    },
}
</script>

<template lang="">
    <div class="container">
        <div class="myrow">
            <div class="col-12 d-flex align-items-center flex-column">
                <h2 class="fw-bold">Our Professional Cycling Trainings</h2>
                <span>Learn from the mountain biking expert.</span>
            </div>
            <div class="container-card d-flex">
                <div class="myCard" v-for="card in proCycling">
                    <div class="card-title fw-bold fs-4">{{card.title}}</div>
                    <img :src=card.image alt="">
                    <button class="view text-white bg-black px-4 py-1">View</button>
                </div>
            </div>
            <div class="col-12 d-flex justify-content-center">
                <button class="my-4 bg-white text-black px-4 mx-1" @click="previus"><i class="fa-solid fa-chevron-left"></i></button>
                <button class="my-4 bg-white text-black px-4 mx-1" @click="next"><i class="fa-solid fa-chevron-right"></i></button>
            </div>
        </div>
    </div>  
</template>

<style lang="scss">
.container-card {
    overflow-x: hidden;
    white-space: nowrap;
}

.myrow {
    margin-top: 200px;
}

.myCard {
    margin: 20px;
    border: solid black 5px;
    position: relative;
    color: white;
}

.card-title {
    position: absolute;
    top: 0;
    left: 0;
    padding: 10px;
    background-color: rgba(0, 0, 0, 0.2);
    width: 100%;
    height: 100%;
}

.view {
    position: absolute;
    left: 10px;
    bottom: 20px;
    display: none;
}

.myCard:hover .view {
    display: block;
}

.myCard:hover .card-title {
    background-color: rgba(0, 0, 0, 0.10);
}
</style>