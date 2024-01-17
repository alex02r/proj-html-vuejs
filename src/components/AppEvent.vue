<script>
export default {
     data() {
          return {

               lista_eventi: [

                    {
                         titolo: 'Toronto Cycling Event 2023',
                         data: "2022-06 - 22 @ 01: 30 - 2024 -08 - 23 @ 07:00",
                         luogo: "Toronto",
                         type: "Bicycle Race",
                         img: "src/assets/event1.jpg"
                    },
                    {
                         titolo: 'Istanbul Cycling Event 2023',
                         data: "2022-06-30 @ 01:30 to 2024-10-19 @ 03:30",
                         luogo: "Istanbul",
                         type: "Bike Sport",
                         img: "src/assets/event2.jpg"
                    },
                    {
                         titolo: 'Paris Cycling Event 2023',
                         data: "2022-06-22 @ 07:30 to 2024-11-08 @ 16:30",
                         luogo: "Paris",
                         type: "Paris",
                         img: "src/assets/event3.jpg"
                    },
                    {
                         titolo: 'New Jersey Cycling Event 2023',
                         data: "2022-06-25 @ 03:00 to 2024-08-24 @ 05:30",
                         luogo: "New Jersey",
                         type: "Bicycle Race",
                         img: "src/assets/event4.jpg"
                    },
                    {
                         titolo: 'Kiev Cycling Event 2023',
                         data: "2022-06-29 @ 10:00 - 2024-05-18 @ 04:30",
                         luogo: "kiev",
                         type: "Bike Sport",
                         img: "src/assets/event5.jpg"
                    },

                    {
                         titolo: '   Colorado Cycling Event 2023',
                         data: "2022-06-28 @ 04:00 - 2024-08-14 @ 05:30",
                         luogo: "Colorado",
                         type: "Bike Sport",
                         img: "src/assets/event6.jpg"
                    },

                    {
                         titolo: ' Amsterdam Cycling Event 2023',
                         data: "2022-06-28 @ 10:30 - 2024-10-24 @ 10:30",
                         luogo: "Amsterdam",
                         type: "Bicycle Race",
                         img: "src/assets/event7.jpg"
                    },
                    {
                         titolo: 'Toronto Cycling Event 2023',
                         data: "2022-06 - 22 @ 01: 30 - 2024 -08 - 23 @ 07:00",
                         luogo: "Toronto",
                         type: "Bicycle Race",
                         img: "src/assets/event8.jpg"
                    },




                    {
                         titolo: 'Paris Cycling Event 2023',
                         data: "2022-06-26 @ 05:30 - 2024-12-20 @ 14:00",
                         luogo: "Paris",
                         type: "Bicycle Race",
                         img: "src/assets/event9.jpg"
                    },




                    {
                         titolo: 'London Cycling Event 2023',
                         data: "2022-06-28 @ 07:30 - 2024-07-26 @ 12:00",
                         luogo: "London",
                         type: "Bike Sport",
                         img: "/src/assets/event10.jpg"
                    }

               ],
               //     console.log('lista_eventi')
          }
     }

}
</script>
<template lang="">
     <div class="container">
          <div class="row">
               <div class="col-12">
                    <div class="text-center">
                              <h2 class="fw-bolder">Don't Miss Our Events!</h2>
                              <h4 class="fw-lighter">Get the amazing cycling experience.</h4>
                    </div>

                    <div class="d-flex justify-content-between mt-5">
                         <h3 class="fw-lighter">Events</h3>
                         <div>
                              <button class="p-1"><i class="fa-solid fa-square"></i></button>
                              <button class="p-1 "><i class="fa-solid fa-bars"></i></button>
                            <!-- :class="bg-dark text-light" -->
                         </div>
                    </div>
               </div>
               <div class="col-4" v-for="eventi, index in lista_eventi">

                    <div class="card mb-3">
                          <img :src="eventi.img" class="card-img-top" alt="...">
                         <div class="card-body">
                              <h5 class="card-title">{{ eventi.titolo }}</h5>
                              <p class="card-text"><p>{{ eventi.data }}</p></p>
                               <p>{{ eventi.luogo }}</p>
                              <a class="btn btn-secondary"><p>{{ eventi.type }}</p></a>
                         </div>
                    </div>
                    
                         
                        
                         

               </div>
          </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/generals.scss' as*;

p{margin: 0;}
</style>