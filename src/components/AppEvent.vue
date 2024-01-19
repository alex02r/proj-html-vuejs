<script>
export default {
     data() {
          return {

               col: true,
               lista_eventi: [

                    {
                         titolo: 'Toronto Cycling Event 2023',
                         data: "2022-06 - 22 @ 01: 30 - 2024 -08 - 23 @ 07:00",
                         giorno_inizio: "22",
                         mese_inizio: "JUN",
                         giorno_fine: "31",
                         mese_fine: "JUN",
                         luogo: "Toronto",
                         type: "Bicycle Race",
                         img: "src/assets/event1.jpg"
                    },
                    {
                         titolo: 'Istanbul Cycling Event 2023',
                         data: "2022-06-30 @ 01:30 to 2024-10-19 @ 03:30",
                         giorno_inizio: "25",
                         mese_inizio: "JUN",
                         giorno_fine: "31",
                         mese_fine: "JUN",
                         luogo: "Istanbul",
                         type: "Bike Sport",
                         img: "src/assets/event2.jpg"
                    },
                    {
                         titolo: 'Paris Cycling Event 2023',
                         data: "2022-06-22 @ 07:30 to 2024-11-08 @ 16:30",
                         giorno_inizio: "22",
                         mese_inizio: "JUN",
                         giorno_fine: "31",
                         mese_fine: "JUN",
                         luogo: "Paris",
                         type: "Bike Sport",
                         img: "src/assets/event3.jpg"
                    },
                    {
                         titolo: 'New Jersey Cycling Event 2023',
                         data: "2022-06-25 @ 03:00 to 2024-08-24 @ 05:30",
                         giorno_inizio: "25",
                         mese_inizio: "JUN",
                         giorno_fine: "31",
                         mese_fine: "JUN",
                         luogo: "New Jersey",
                         type: "Bicycle Race",
                         img: "src/assets/event4.jpg"
                    },
                    {
                         titolo: 'Kiev Cycling Event 2023',
                         data: "2022-06-29 @ 10:00 - 2024-05-18 @ 04:30",
                         giorno_inizio: "29",
                         mese_inizio: "JUN",
                         giorno_fine: "31",
                         mese_fine: "JUN",
                         luogo: "kiev",
                         type: "Bike Sport",
                         img: "src/assets/event5.jpg"
                    },

                    {
                         titolo: '   Colorado Cycling Event 2023',
                         data: "2022-06-28 @ 04:00 - 2024-08-14 @ 05:30",
                         giorno_inizio: "28",
                         mese_inizio: "JUN",
                         giorno_fine: "31",
                         mese_fine: "JUN",
                         luogo: "Colorado",
                         type: "Bike Sport",
                         img: "src/assets/event6.jpg"
                    },

                    {
                         titolo: ' Amsterdam Cycling Event 2023',
                         data: "2022-06-28 @ 10:30 - 2024-10-24 @ 10:30",
                         giorno_inizio: "28",
                         mese_inizio: "JUN",
                         giorno_fine: "31",
                         mese_fine: "JUN",
                         luogo: "Amsterdam",
                         type: "Bicycle Race",
                         img: "src/assets/event7.jpg"
                    },
                    {
                         titolo: 'Toronto Cycling Event 2023',
                         data: "2022-06 - 22 @ 01: 30 - 2024 -08 - 23 @ 07:00",
                         giorno_inizio: "22",
                         mese_inizio: "JUN",
                         giorno_fine: "31",
                         mese_fine: "JUN",
                         luogo: "Toronto",
                         type: "Bicycle Race",
                         img: "src/assets/event8.jpg"
                    },




                    {
                         titolo: 'Paris Cycling Event 2023',
                         data: "2022-06-26 @ 05:30 - 2024-12-20 @ 14:00",
                         giorno_inizio: "26",
                         mese_inizio: "JUN",
                         giorno_fine: "31",
                         mese_fine: "JUN",
                         luogo: "Paris",
                         type: "Bicycle Race",
                         img: "src/assets/event9.jpg"
                    },




                    {
                         titolo: 'London Cycling Event 2023',
                         data: "2022-06-28 @ 07:30 - 2024-07-26 @ 12:00",
                         giorno_inizio: "28",
                         mese_inizio: "JUN",
                         giorno_fine: "31",
                         mese_fine: "JUN",
                         luogo: "London",
                         type: "Bike Sport",
                         img: "/src/assets/event10.jpg"
                    }

               ],
          }

          
     }

}
</script>
<template lang="">
     <div class="container" v-motion :delay="200" :initial="{ opacity: 0, y: 100}" :visibleOnce="{ opacity: 1, y: 0}">
          <div class="row">
               <div class="col-12">
                    <div class="text-center">
                              <h2 class="fw-bolder">Don't Miss Our Events!</h2>
                              <h4 class="fw-lighter">Get the amazing cycling experience.</h4>
                    </div>

                    <div class="d-flex justify-content-between mt-5">
                         <h3 class="fw-lighter">Events</h3>
                         <div class="buttons">
                              <button class="p-2" @click="col = true"><i class="fa-solid fa-square"></i></button>
                              <button class="p-2 " @click="col = false"><i class="fa-solid fa-bars"></i></button>
                            <!-- :class="bg-dark text-light" -->
                         </div>
                    </div>
               </div>
               <div :class="col ? 'col-4 mt-4' : 'col-12'" v-for="eventi, index in lista_eventi">

                    <div class="carta mb-3">
                          <img :src="eventi.img" class="" alt="...">
                          <div class="data">
                              <span>{{ eventi.giorno_inizio }}</span>
                              <p>{{ eventi.mese_inizio }}</p>
                          </div>

                          <div class="inizio_fine">
                               
                               <div>{{ eventi.giorno_inizio }} - {{ eventi.giorno_fine }}</div>
                                   <span class="mese-1">{{ eventi.mese_inizio }}</span> <span class="mese-2">{{ eventi.mese_inizio }}</span>
                          </div>

                         <div class="card-b py-3">
                              <h5 class="card-title">{{ eventi.titolo }}</h5>
                              <p class="card-text py-2"><i class="fa-regular fa-clock"></i> {{ eventi.data }}</p>
                              <p><i class="fa-solid fa-location-dot"></i> {{ eventi.luogo }}</p>
                              <a class="btn btn-crema mt-2">{{ eventi.type }}</a>
                         </div>
                    </div>
                    
                         
                        
                         

               </div>
          </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/partial/variables' as *;
@use '../styles/generals.scss';


.btn-crema {
     background-color: $grey;
}

.buttons{
     button{
          border: none;
     }
}
.col-12{

     .carta{
          display: flex;
          justify-content: space-between;
          height: 200px;
          border: 1px solid rgb(199, 199, 199);
          border-radius: 10px;

           &:hover{
               scale: 0.99;
          }
          .data{
               display: none;
          }

          .card-b{
               margin-right: 30px;
               margin-top: 30px;
          }
          img{
               padding: 10px;
               width: 50%;
               overflow: hidden;
               object-fit: cover;
              
          }
          .inizio_fine{
               margin-top: 30px;
               div{
                    font-size: 80px;

               }
               .mese-1{
                    position: relative;
                    bottom: 20px;
                    font-size: 15px;
                    margin-left:35px ;
               }
               .mese-2{
                    position: relative;
                    bottom: 20px;
                    font-size: 15px;
                    margin-left:110px ;
               }
     }
     }
}



.col-4{
     .carta{
          .inizio_fine{
          display: none;
          }
     }
}
.carta {
     position: relative;
     border: 1px solid rgb(199, 199, 199);
     border-radius: 5px;
     .card-b{
          margin-left: 10px;
     }
     img{
          max-width: 100%;
     }

     .data {
          padding: 0px 15px;
          position: absolute;
          top: 10px;
          left: 10px;
          background-color: $white;
          border-radius: 8px;

          span{
               font-size: 25px;
          }
          p{
               font-size: 15px;
               position: relative;
               bottom: 10px;
               right: 2px;
               color: grey;
          }
     }
     
}

p {
     margin: 0;
}

</style>