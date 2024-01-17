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

                        <!-- Fronte della card -->
                        <div class="front-card">
                            <i class="fa-regular fa-handshake"></i>
                            <h3 class="fw-bolder">Basic</h3>
                            <p>Learn to ride a bike from the professionals</p>
                            <ul>
                                <li v-for="index in li_packs" :key="index">
                                    {{index}}
                                </li>
                            </ul>
                        </div>

                        <!-- Retro della card -->
                        <div class="retro-card">
                            <h4 class="text-light text-uppercase fw-bolder">basic</h4>
                            <p class="fw-bolder">$1800</p>
                            <button class="fw-bolder">Send Request!</button>
                        </div>
                    </div>


                    <!-- Pacchetto Standard -->
                    <div class="col-3 packages text-center">

                        <!-- Fronte della card -->
                        <div class="front-card">
                            <i class="fa-regular fa-handshake"></i>
                            <h3 class="fw-bolder">Standard</h3>
                            <p>Learn to ride a bike from the professionals</p>
                            <ul>
                                <li v-for="index in li_packs" :key="index">
                                    {{index}}
                                </li>
                            </ul>
                        </div>

                        <!-- Retro della card -->
                        <div class="retro-card">
                            <h4 class="text-light text-uppercase fw-bolder">Standard</h4>
                            <p class="fw-bolder">$2500</p>
                            <button class="fw-bolder">Send Request!</button>
                        </div>
                    </div>

                    <!-- Pacchetto Premium -->
                    <div class="col-3 packages text-center">

                        <!-- Fronte della card -->
                        <div class="front-card">
                            <i class="fa-regular fa-handshake"></i>
                            <h3 class="fw-bolder">Premium</h3>
                            <p>Learn to ride a bike from the professionals</p>
                            <ul>
                                <li v-for="index in li_packs" :key="index">
                                    {{index}}
                                </li>
                            </ul>
                        </div>

                        <!-- Retro della card -->
                        <div class="retro-card">
                            <h4 class="text-light text-uppercase fw-bolder">Premium</h4>
                            <p class="fw-bolder">$5000</p>
                            <button class="fw-bolder">Send Request!</button>
                        </div>
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
        height: 500px;
        margin: 30px;
        position: relative;

        &:hover .front-card {
            display: none;
        }

        &:hover .retro-card {
            display: block;
        }

        .front-card {
            display: block;
            width: 100%;
            height: 100%;
            background-color: $black;
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

        .retro-card {
            background-color: $black;
            position: absolute;
            top: 0;
            left: 0;
            display: none;
            width: 100%;
            height: 100%;
            padding: 40% 0;
            border-radius: 5px;

            h3 {
                margin: 40px;
            }

            p {
                color: $white;
                font-size: 40px;
            }

            button {
                margin-top: 50px;
                padding: 20px;
                background-color: black;
                color: $white;
                border-radius: 5px;
            }
        }
    }

}
</style>