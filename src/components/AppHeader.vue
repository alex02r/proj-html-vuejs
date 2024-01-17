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
                <ul>
                    <li v-for="(item, index) in menu" :key="index" >{{item}}</li>
                </ul>
            </div>
            <div class="headerCol d-flex justify-content-end ">
                <div class="hamburgerMenu"><i class="fas fa-bars"></i></div>
                <div>Upcoming Events<i class="fas fa-arrow-right"></i></div>
            </div>
        </div>
    </div>
</header>
</template>

<style lang="scss">
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
}
</style>