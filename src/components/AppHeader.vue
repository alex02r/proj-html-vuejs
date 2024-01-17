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
                <ul class="d-flex list-unstyled">
                    <li class="fw-bold mx-2 px-1" v-for="(item, index) in menu" :key="index" >{{item}}</li>
                </ul>
            </div>
            <div class="headerCol d-flex justify-content-end ">
                <div class="hamburgerMenu">
                    <i class="fas fa-bars"></i>
                </div>
                <div class="bg-black text-light btn-padding fw-bold ">
                    <i class="fas fa-helmet-safety text-light"></i>
                    <a class="text-decoration-none text-light" href="" >Upcoming Events<i class="fas fa-arrow-right text-light"></i></a>
                </div>
            </div>
        </div>
    </div>
</header>
</template>

<style lang="scss" scoped>
header{
    height: 120px;
    background-color: white;

    .headerCol{
        width: calc(100% / 3);
        height: 100%;
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