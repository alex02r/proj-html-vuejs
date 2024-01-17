<script>
export default {
    name: 'CardContainer',
    data() {
        return {
            li_packs: [
                'Phone Mountainer bike training',
                'Remote Excellent bike server',
                'Onsite Safe cycling training',
                'Safety helmet on bike',
                'Free bikes for children'
            ]
        }
    }
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
                

                <!-- Card pacchetto abbonamenti -->
                <div class="d-flex justify-content-center">

                    <!-- Pacchetto Basic -->
                    <div class="col-3 packages text-center">
                        <i class="fa-regular fa-handshake"></i>
                        <h3 class="fw-bolder">Basic</h3>
                        <p>Learn to ride a bike from the professionals</p>
                        <ul>
                            <li v-for="index in li_packs" :key="index">
                                {{index}}
                            </li>
                        </ul>
                    </div>

                    <!-- Pacchetto Standard -->
                    <div class="col-3 packages">
                        
                    </div>

                    <!-- Pacchetto Premium -->
                    <div class="col-3 packages">
                        
                    </div>
                </div>
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

    .packages {
        background-color: $black;
        margin: 40px;
        padding: 20px 10px;
        border-radius: 5px;

        i {
            color: $white;
            font-size: 50px;
        }

        h3 {
            margin-top: 30px;
            color: $white;
            font-size: 20px;
        }

        p {
            color: $white;
            font-size: 15px;
            margin-top: 15px;
        }

        ul {
            color: $white;
            list-style: none;
            margin-top: 30px;

            li {
                font-size: 15px;
                padding: 10px;
                margin: 0;
                border-bottom: 1px solid grey;
            }
        }
    }
}
</style>