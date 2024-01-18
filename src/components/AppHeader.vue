<script>
export default {
    name: 'AppHeader',

    props:{
        menu: Array,
    }
}
</script>

<template lang="">
<header>
    <div class='container'>
        <div class="row align-items-center ">
            <div class="headerCol">
                <div class="logo">
                    <img src="../assets/logo-gobike.png" alt="">
                </div>
            </div>
            <div class="headerCol d-flex justify-content-center">
                <ul class="m-0 d-flex list-unstyled">
                    <li class="fw-bold mx-1 px-1 fs-5" v-for="(item, index) in menu" :key="index" ><a class="text-decoration-none text-dark " href="#">{{item}}</a></li>
                </ul>
            </div>
            <div class="headerCol d-flex justify-content-end ">
                <div class="hamburgerMenu d-flex  align-items-center px-4 fs-2 ">
                    <a class="text-decoration-none text-dark" href="#"><i class="fas fa-bars"></i></a>
                </div>
                <div class="bg-black text-light btn-padding fw-bold d-flex align-items-center ">
                    <a href="#"><i class="fas fa-helmet-safety text-light fs-2 pe-4"></i></a>
                    <a class="text-decoration-none text-light fs-5" href="#" >Upcoming Events<i class="fas fa-arrow-right text-light ms-2 fs-5"></i></a>
                </div>
            </div>
        </div>
    </div>
</header>
</template>

<style lang="scss" scoped>
header{
    width: 100%;
    height: 110px;
    background-color: white;
    position: fixed;
    z-index: 1;

    .headerCol{
        width: calc(100% / 3);
        height: 100%;

        li{
            a{
                position: relative;
            }
            a::after{
                content: "";
                position: absolute;
                bottom: -8px;
                height: 3px;
                width: 100%;
                left: 0;
                background-color: black;
                transition: 0.3s;
                transition-timing-function: ease-in-out;
                transform: scaleX(0);
            }
            a:hover::after{
                transform: scaleX(1);
            }
        }
    }

    .logo{
        img{
            width: 300px;
        }
    }

    .btn-padding{
        padding: 20px 40px;
    }
}
</style>