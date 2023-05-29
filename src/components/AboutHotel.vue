<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Autoplay, Pagination, Navigation } from 'swiper';
const modules = [Autoplay, Pagination, Navigation]

</script>
<template>
   <div class="about">
      <div class="line">
         <img class="line2" src="@/assets/line.svg" alt="">
      </div>
      <h5>See Our Review</h5>
      <h2>What Our User Say About Us</h2>
      <swiper :pagination="true" :spaceBetween="30" :slides-per-view="2.2" :centeredSlides="false" :autoplay="{
         delay: 150000,
      }" :breakpoints="{
   '@0.05': {
      slidesPerView: 1,
      spaceBetween: 10,
   },
   '@0.75': {
      slidesPerView: 1.3,
      spaceBetween: 10,
   },
   '@1.00': {
      slidesPerView: 1.8,
      spaceBetween: 10,
   },

   '@1.50': {
      slidesPerView: 2.3,
      spaceBetween: 40,
   }
}" :modules="modules" class="mySwiper1">
         <swiper-slide v-for="item in 9" :key="item">
            <div class="carusel_card">
               <img class="gallery" src="@/assets/about.png" alt="">
               <div class="box">
                  <h4>Best! I got the house I wanted through Hounter</h4>
                  <p class="text">Through this website I can get a house with the type and specifications I want very
                     easily,
                     without a complicated process to be able to find information on the house we want.</p>
                  <div class="box_star">
                     <div class="box_star_left">
                        <img src="@/assets/vid.svg" alt="">
                        <div class="box_item">
                           <h3>Dianne Russell</h3>
                           <p>
                              Manager Director
                           </p>
                        </div>
                     </div>
                     <div class="box_star_right">
                        <img src="@/assets/star.svg" alt="">
                        <strong>4.6</strong>
                     </div>
                  </div>
               </div>
            </div>
         </swiper-slide>

      </swiper>
   </div>
</template>


<style lang="scss" >
.about {
   margin-top: 100px;

   .swiper {
      padding-bottom: 60px !important;
   }

   .swiper-horizontal>.swiper-pagination-bullets,
   .swiper-pagination-bullets.swiper-pagination-horizontal,
   .swiper-pagination-custom,
   .swiper-pagination-fraction {
      z-index: 9999;
      bottom: 5px !important;
   }

   .line {
      margin: 10px 0;
      display: flex;
      align-items: center;
      justify-content: center;
   }

   h5 {
      font-family: 'Lexend';
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;
      text-align: center;
      text-transform: capitalize;

      color: #F59E0B;
   }

   h2 {
      font-family: 'Lexend';
      font-style: normal;
      font-weight: 600;
      font-size: 32px;
      line-height: 40px;
      text-align: center;
      text-transform: capitalize;
      color: #1B1C57;
      margin-top: 16px;
      margin-bottom: 40px;
   }

   .carusel_card {

      .gallery {
         width: 100%;
      }
   }

   .box {
      position: relative;
      z-index: 99;
      padding: 32px;
      background: #FFFFFF;
      box-shadow: 0px 9px 32px rgba(89, 92, 219, 0.05);
      border-radius: 16px;
      margin: 0px 50px;
      margin-top: -150px;

      h4 {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 600;
         font-size: 20px;
         line-height: 25px;
         text-transform: capitalize;
         color: #1B1C57;

      }

      .text {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 400;
         font-size: 14px;
         line-height: 24px;
         color: #626687;
         opacity: 0.75;
         margin-top: 20px;
         margin-bottom: 26px;
      }
   }

   .box_star {

      display: flex;
      align-items: center;
      justify-content: space-between;

      h3 {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 500;
         font-size: 14px;
         line-height: 22px;
         color: #0E1735;
      }

      p {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 500;
         font-size: 14px;
         line-height: 22px;
         color: #888B97;
      }
   }

   .box_star_left {
      display: flex;
      gap: 15px;
      align-items: center;
   }

   .box_star_right {
      display: flex;
      gap: 8px;

      strong {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 600;
         font-size: 20px;
         line-height: 28px;
         color: #3C4563;
      }
   }

   @media(max-width: 1024px) {
      .box {
         margin: 0px 20px;
         margin-top: -100px;
         padding: 16px;

         h4 {
            font-size: 16px;
         }

         .text {
            font-weight: 300;
            margin-top: 6px;
            line-height: 1.5;
         }

         .box_star_left {
            img {
               width: 46px;
               height: 46px;
            }
         }
      }
   }

   @media(max-width: 556px) {
      margin-top: 40px;
      padding: 0px 16px;
      h2 {
         font-size: 24px;
         line-height: 1.4;
      }

      .box {
         margin: 0px;
         padding: 0;
      }
   }
}
</style>