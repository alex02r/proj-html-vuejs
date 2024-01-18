<script>
export default {

}
</script>

<template lang="">
    <div class="margin-top"></div>
    <div class="container">
        <div class="row">
            <div class="col-8">
                <div class="bike">
                    <img class="bike-player play" src="../assets/bike-circle.png" alt="">
                    <img class="bike-player" src="../assets/bike-player.png" alt="">
                </div>
            </div>
            <div class="col-4">
                <h2 class="fw-bold">Do you want to be a professional cyclist?</h2>
                <p>We offer 6 courses of varying difficulty and beautiful scenery that cyclists of all levels can enjoy. You will learn cycling from professionals with our competent and experienced staff. You will have a lot of fun with our amazing space.
                    <br>
                    <img src="../assets/divider.jpg" alt="divider" class="w-25">
                </p>
                <div class="paragraph">
                    <img class="icon" src="https://cdn-icons-png.flaticon.com/128/882/882115.png"  alt="">
                    <div>
                        <h3 class="fw-bold">Professional Team</h3>
                        <p>We make you professional by adding your sincerity as well as professionalism.</p>
                    </div>
                </div>
                <div class="paragraph">
                    <img class="icon" src="https://cdn-icons-png.flaticon.com/128/972/972998.png" alt="">
                    <div>
                        <h3 class="fw-bold">Professional Trainings</h3>
                        <p>We always ride with the best equipment, respecting nature and fun.</p>
                    </div>
                </div>
                <button class="text-center mt-4">Get to know us <i class="fa-solid fa-arrow-right p-2"></i></button>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partial/variables' as *;
.margin-top{
    margin: 200px 0;
}
.bike {
    height: 100%;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    .bike-player {
        position: absolute;
        width: 80%;
    }
    .play{
        animation-name: ruota;
        animation-duration: 8000ms;
        animation-timing-function: linear;
        animation-iteration-count: infinite;
    }
}
button {
    padding: 20px 50px;
    font-weight: bold;
    background-color: $black;
    color: $white;
}
.paragraph{
    display: flex;
    align-items: center;
    gap: 20px;
    .icon{
        width: 70px;
        height: 70px;
    }
}
@keyframes ruota {
    from { 
        transform:rotate(0deg);
    }
    to {
        transform:rotate(360deg);
    }
}
</style>