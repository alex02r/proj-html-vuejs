<script>
export default {
    name: 'CardContainer',
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
                    image: '/src/news-bike5-300x180.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'Road bike or mountain bike?',
                    text: 'Compared to similar road bikes with a solid frame structure. [...]'
                },
                {
                    image: '/src/news-bike6-300x180.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'What is mountain biking called?',
                    text: 'Mountain biking is one of the most popular outdoor sports. [...]'
                },
                {
                    image: '/src/news-bike3-300x180.jpg',
                    date: '22.06.2022 - Bike',
                    title: 'How much shoul you cycle a day?',
                    text: 'In order to get the right benefit from the exercise. [...]'
                },
                {
                    image: '/src/news-bike4-300x180.jpg',
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
                <span class="text-center">Select pricing plan to get more</span>
                

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


                    <!-- Pacchetto Standard -->
                    <div class="col-3 packages text-center">

                        <!-- Fronte della card -->
                        <div class="front-card">
                            <i class="fa-regular fa-handshake"></i>
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

                    <!-- Pacchetto Premium -->
                    <div class="col-3 packages text-center">

                        <!-- Fronte della card -->
                        <div class="front-card">
                            <i class="fa-regular fa-handshake"></i>
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
    </section>

    <!-- Sezione New Articles -->
    <section class="new-articles">
        <div class="container">
            <div class="row">
                <h2 class="fw-bolder text-center">Resent New & Articles</h2>
                <span class="text-center">Select pricing plan to get more</span>

                <!-- Card -->
                <div class="cards d-flex justify-content-center">
                    <div class="col-3" v-for="(card, index) in new_articles" :key="index">
                        <div class="card mx-4">
                            <!-- <img :src="{{card.image}}" class="" alt="{{card.title}}"> -->
                            <div class="card-body">
                                <p class="text-center">{{card.date}}</p>
                                <h4 class="text-center">{{card.title}}</h4>
                                <p class="text-center mt-5">{{card.text}}</p> 
                                <div class="d-flex justify-content-center">
                                    <button class="my-2">More</button>
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
            padding: 20px 0;
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
                margin-top: 80px;
                padding: 0 30px;

                li {
                    font-size: 15px;
                    padding: 10px;
                    margin: 10px 0;
                    border-bottom: 1px solid grey;

                    i {
                        font-size: 20px;
                    }
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

.new-articles {
    padding: 50px 0;
    background-color: $grey;

    .cards {
        margin-top: 20px;

        .card {
            box-shadow: 0 0 10px 5px $grey;

            button {
                width: 50%;
                padding: 20px;
                background-color: black;
                color: $white;
            }
        }

    }
}
</style>