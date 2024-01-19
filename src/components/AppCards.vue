<script>
import AppTrainers from './AppTrainers.vue';
export default {
    name: 'AppCards',
    components: {
        AppTrainers
    },
    data() {
        return {
            li_packs: [
                {
                    name: 'Phone Mountainer bike training',
                    done: true,
                },
                {
                    name: 'Remote Excellent bike server',
                    done: true,
                },
                {
                    name: 'Onsite Safe cycling training',
                    done: true,
                },
                {
                    name: 'Safety helmet on bike',
                    done: false,
                },
                {
                    name: 'Free bikes for children',
                    done: false,
                },
            ],
            new_articles: [
                {
                    image: '/src/assets/news-bike5-300x180.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'Road bike or mountain bike?',
                    text: 'Compared to similar road bikes with a solid frame structure. [...]'
                },
                {
                    image: '/src/assets/news-bike6-300x180.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'What is mountain biking called?',
                    text: 'Mountain biking is one of the most popular outdoor sports. [...]'
                },
                {
                    image: '/src/assets/news-bike3-300x180.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'How much shoul you cycle a day?',
                    text: 'In order to get the right benefit from the exercise. [...]'
                },
                {
                    image: '/src/assets/news-bike4-300x180.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'How long does it take 5 km by bike?',
                    text: 'It takes 5 km and 10 minutes. sir. But at. [...]'
                },
            ]
        }
    }
}   
</script>

<template lang="">
    <AppTrainers/>
    <!-- Sezione Special Packs-->
    <section class="special-packs">
        <div class="container">
            <div class="row">
                <div class="d-flex justify-content-center">
                    <div class="medal-square d-flex justify-content-center align-items-center">
                        <img class="icon" src="https://cdn-icons-png.flaticon.com/512/1851/1851036.png" alt="">
                    </div>
                </div>
                <h2 class="fw-bolder text-center mt-3">Special Packs</h2>
                <span class="text-center">Select pricing plan to get more</span>
                

                <!-- Card pacchetto abbonamenti -->
                <div class="d-flex justify-content-center">

                    <!-- Pacchetto Basic -->
                    <div class="col-4">
                        <div class="packages text-center" v-motion :initial="{ opacity: 0, x: -100}" :visibleOnce="{ opacity: 1, x: 0, transition:{ duration: 800},}">
                            <div class="inner-card">

                                <!-- Fronte della card -->
                                <div class="front-card">
                                    <img class="icon" src="https://cdn-icons-png.flaticon.com/128/3562/3562049.png" alt="">
                                    <h3 class="fw-bolder">Basic</h3>
                                    <p>Learn to ride a bike from the professionals</p>
                                    <ul>
                                        <li v-for="item, index in li_packs" :key="index">
                                            <div class="d-flex align-items-center justify-content-center">
                                                <i :class="item.done == true ? 'fa-solid fa-check' : 'fa-solid fa-xmark'"></i>
                                                <span class="ms-2">{{item.name}}</span>
                                            </div>
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
                        </div>
                    </div>

                    <!-- Pacchetto Standard -->
                    <div class="col-4">

                        <div class="packages text-center" v-motion :initial="{ opacity: 0, x: -100}" :visibleOnce="{ opacity: 1, x: 0, transition:{ duration: 900},}">
                            <div class="inner-card">

                                <!-- Fronte della card -->
                                <div class="front-card">
                                    <img class="icon" src="https://cdn-icons-png.flaticon.com/128/972/972998.png" alt="">
                                    <h3 class="fw-bolder">Standard</h3>
                                    <p>Learn to ride a bike from the professionals</p>
                                    <ul>
                                        <li v-for="item, index in li_packs" :key="index">
                                            <div class="d-flex align-items-center justify-content-center">
                                                <i :class="item.done == true ? 'fa-solid fa-check' : 'fa-solid fa-xmark'"></i>
                                                <span class="ms-2">{{item.name}}</span>
                                            </div>
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
                        </div>
                    </div>

                    <!-- Pacchetto Premium -->
                    <div class="col-4">
                        <div class="packages text-center" v-motion :initial="{ opacity: 0, x: -100}" :visibleOnce="{ opacity: 1, x: 0, transition:{ duration: 1000},}">

                            <div class="inner-card">
                                <!-- Fronte della card -->
                                <div class="front-card">
                                    <img class="icon" src="https://cdn-icons-png.flaticon.com/128/882/882115.png" alt="">
                                    <h3 class="fw-bolder">Premium</h3>
                                    <p>Learn to ride a bike from the professionals</p>
                                    <ul>
                                        <li v-for="item, index in li_packs" :key="index">
                                            <div class="d-flex align-items-center justify-content-center">
                                                <i :class="item.done == true ? 'fa-solid fa-check' : 'fa-solid fa-xmark'"></i>
                                                <span class="ms-2">{{item.name}}</span>
                                            </div>
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
            </div>
        </div>
    </section>

    <!-- Sezione New Articles -->
    <section class="new-articles my-padding">
        <div class="container">
            <div class="row">
                <h2 class="fw-bolder text-center">Resent New & Articles</h2>
                <span class="text-center" v-motion :initial="{ opacity: 0, y: 100}" :visibleOnce="{ opacity: 1, y: 0}">Select pricing plan to get more</span>

                <!-- Card -->
                <div class="cards d-flex justify-content-center" v-motion :initial="{ opacity: 0, x: -100}" :visibleOnce="{ opacity: 1, x: 0, transition:{ duration: 1000},}">
                    <div class="col-3" v-for="(card, index) in new_articles" :key="index">
                        <div class="card mx-4 shadow h-100">
                            <div class="pt-3 px-3">
                                <img  class="card-img-top" :src="card.image" :alt="card.title">
                                <p class="text-center">{{card.date}}</p>
                            </div>
                            <div class="card-body">
                                <h5 class="text-center fw-bold">{{card.title}}</h5>
                                <p class="mt-3">{{card.text}}</p> 
                                <div class="d-flex justify-content-center">
                                    <button class="my-2 border border-0 rounded-1">More</button>
                                </div>
                            </div>
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
    margin: 50px 0;

    .medal-square {
        width: 100px;
        height: 100px;
        background-color: $black;
        border-radius: 5px;

        .icon {
            width: 50px;
            filter: invert(100%);
        }
    }

    .packages {
        height: 600px;
        margin: 30px;
        perspective: 1000px;

        &:hover .inner-card {
            transform: rotateY(180deg);
        }

        .inner-card {
            height: 100%;
            width: 100%;
            position: relative;
            transition: transform 0.6s;
            transform-style: preserve-3d;

            .front-card {
                display: block;
                width: 100%;
                height: 100%;
                background-image: linear-gradient(175deg, black 40%, white 40%);
                box-shadow: 0 0 10px 5px $grey;
                padding: 20px 0;
                border-radius: 5px;
                -webkit-backface-visibility: hidden;
                backface-visibility: hidden;

                .icon {
                    width: 50px;
                    filter: invert(100%);
                }

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
                    list-style: none;
                    margin: 80px 0;
                    padding: 0 30px;

                    li {
                        font-size: 15px;
                        padding: 10px;
                        margin: 10px 0;
                        border-bottom: 1px solid lightgray;

                        i {
                            font-size: 15px;
                            color: black;
                        }
                    }
                }
            }

            .retro-card {
                background-color: $black;
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                padding: 40% 0;
                border-radius: 5px;
                transform: rotateY(180deg);
                -webkit-backface-visibility: hidden;
                backface-visibility: hidden;

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

        .card-body {
            p {
                color: $grey;
            }
        }

    }

}

.new-articles {
    padding-top: 50px;
    padding-bottom: 150px;
    background-color: $grey;

    .cards {
        margin-top: 20px;

        .card {
            box-shadow: 0 0 10px 5px $grey;

            .card-body {
                button {
                    width: 50%;
                    padding: 20px;
                    background-color: black;
                    color: $white;
                }

                p {
                    color: #545454;
                    font-size: 15px;
                }
            }

        }

    }
}
</style>