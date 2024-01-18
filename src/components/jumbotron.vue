<script>
export default {

}
</script>

<template lang="">
    <div class="container">
        <div class="row">
            <div class="padding-200"></div>
            <div class="col-8">
                <div class="bike d-flex justify-content-end ">
                <img class="bike-player" src="../assets/bike-circle.png" alt="">
                <img class="bike-player" src="../assets/bike-player.png" alt="">
                </div>
            </div>
            <div class="col-4">
                <h2 class="fw-bold">Do you want to be a professional cyclist?</h2>
                <p>We offer 6 courses of varying difficulty and beautiful scenery that cyclists of all levels can enjoy. You will learn cycling from professionals with our competent and experienced staff. You will have a lot of fun with our amazing space.</p>
                <div class="d-flex my-5">
                    <img class="w-h-20 mx-3" src="https://cdn-icons-png.flaticon.com/128/1275/1275364.png"  alt="">
                    <div>
                    <h3 class="fw-bold">Professional Team</h3>
                    <p>We make you professional by adding your sincerity as well as professionalism.</p>
                    </div>
                </div>
                <div class="d-flex my-5">
                    <img class="w-h-20 mx-3" src="https://cdn-icons-png.flaticon.com/128/972/972998.png" alt="">
                    <div>
                    <h3 class="fw-bold">Professional Trainings</h3>
                    <p>We always ride with the best equipment, respecting nature and fun.</p>
                    </div>
                </div>
                <button class="d-flex alin align-items-center">Get to know us <i class="fa-solid fa-arrow-right p-2"></i></button>
            </div>
            <div class="padding-200"></div>
        </div>
        
    </div>
</template>

<style lang="scss">
.bike {
    width: 100%;
    position: relative;
    padding-right: 50px;
}

.bike-player {
    position: absolute;
    width: 70%;
}

button {
    padding: 20px 50px;
    font-weight: bold;
    background-color: black;
    color: white;
}

.padding-200 {
    padding-top: 200px;
}

.w-h-20 {
    width: 20%;
    height: 20%;
}
</style>