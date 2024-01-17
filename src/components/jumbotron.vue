<script>
export default {

}
</script>

<template lang="">
    <div class="mycontainer">
        <div class="myrow d-flex">
            <div class="col60 d-flex justify-content-end ">
                <img class="bike-circle" src="../assets/bike-circle.png" alt="">
                <img class="bike-player" src="../assets/bike-player.png" alt="">
            </div>
            <div class="col40">
                <h2 class="fw-bold">Do you want to be a professional cyclist?</h2>
                <p>We offer 6 courses of varying difficulty and beautiful scenery that cyclists of all levels can enjoy. You will learn cycling from professionals with our competent and experienced staff. You will have a lot of fun with our amazing space.</p>
                <h3 class="fw-bold">Professional Team</h3>
                <p>We make you professional by adding your sincerity as well as professionalism.</p>
                <h3 class="fw-bold">Professional Trainings</h3>
                <p>We always ride with the best equipment, respecting nature and fun.</p>
                <button>Get to know us</button>
            </div>
        </div>
        
    </div>
</template>

<style lang="scss">
.col60 {
    width: 60%;
    position: relative;
    padding-top: 80px;
    padding-right: 100px;
}

.col40 {
    width: 20%;
    padding-top: 100px;
    padding-left: 20px;
    font-size: 15px;
}

.bike-player {
    position: absolute;
    bottom: 20px;
    top: 30px;
    right: 0px;
    left: 250px;
    width: 60%;

}

.bike-circle {
    width: 70%;
    height: 90%;
}


button {
    padding: 20px;
    font-weight: bold;
    background-color: black;
    color: white;
}
</style>