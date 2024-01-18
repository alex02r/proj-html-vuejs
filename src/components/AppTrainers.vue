<script>
export default {
    name: 'AppTrainers',

    data() {
        return {
            trainersList: [
                {
                    img: '/src/assets/biker1.jpg',
                    name: 'Michael Lee',
                    role: 'Biker'
                },
                {
                    img: '/src/assets/biker2.jpg',
                    name: 'Robert Lee',
                    role: 'Biker'
                },
                {
                    img: '/src/assets/biker3.jpg',
                    name: 'John Doe',
                    role: 'Biker'
                },
                {
                    img: '/src/assets/biker4.jpg',
                    name: 'Emily Brown',
                    role: 'Biker'
                }
            ]
        }
    },
}
</script>

<template lang="">
    <div class="container py-5">
        <div class="row">
            <div class="col-12 text-center">
                <h2 class="fw-bold ">Our Expert Trainers</h2>
                <p class="text-secondary">Learn to ride a bike from the experts</p>
            </div>
            <div class="col-3" v-for="(item, index) in trainersList" :key="index" >
                <div class="my-card">
                    <div class="img-area">
                        <img :src="item.img" alt="">
                    </div>
                    <div class="my-card-text">
                        <div class="trainers-name fw-bold ">{{item.name}}</div>
                        <div class="role text-secondary">{{item.role}}</div>
                        <div>
                            <a href="#"><i class="fab fa-facebook-f"></i></a>
                            <a href="#"><i class="fab fa-instagram-square"></i></a>
                            <a href="#"><i class="fab fa-twitter"></i></a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.my-card{
    position: relative;
    cursor: pointer;
    .my-card-text{
        padding: 20px 0;
        text-align: center;
        width: 100%;
        height: 120px;
        position: absolute;
        background-color: black;
        color: white;
        bottom: 0;
        transition: height 0.8s;
        a{
            margin: 0 10px;
            color: white;
        }
    }
    .img-area{
        width: 100%;
        height: 100%;
        overflow: hidden;
        img{
            transition: 0.8s;
            border-radius: 5px;
            width: 100%;
        }

    }
    .trainers-name{
        font-size: 20px;
    }
    .role{
        margin-bottom: 5px;
    }
}
.my-card:hover{
    .my-card-text{
        height: 140px;
    }

    img{
        transform: scale(1.2);
        filter: brightness(0.5);
    }
}
</style>