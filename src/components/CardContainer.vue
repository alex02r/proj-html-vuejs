<script>
export default {
    name: 'CardContainer',
}   
</script>

<template lang="">

    <!-- Sezione Special Packs-->
    <section class="special-packs">
        <div class="container">
            <div class="row">
                <div class="d-flex justify-content-center">
                    <div class="medal-square d-flex justify-content-center align-items-center">
                        <i class="fa-solid fa-medal"></i>
                    </div>
                </div>
                <h2 class="fw-bolder text-center mt-3">Special Packs</h2>
                <p class="text-center">Select pricing plan to get more</p>
            </div>
        </div>
    </section>
    
</template>

<style lang="scss" scoped>
@use '../styles/partial/variables' as *;

.special-packs {
    padding: 20px;

    .medal-square {
        width: 100px;
        height: 100px;
        background-color: $black;
        border-radius: 5px;

        i {
            color: $white;
            font-size: 50px;
        }
    }
}
</style>