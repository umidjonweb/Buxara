<script setup>
import { ref } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';

// import './style.css';

import { Autoplay, Pagination, Navigation } from 'swiper';

const isBurger = ref(true)
const modules = [Autoplay, Pagination, Navigation]

</script>
<template>
   <div class="header">
      <div class="container">
         <img v-if="isBurger" src="@/assets/logo1.png" alt="">
         <nav v-if="isBurger">
            <li><a class="active" href="#">Home</a> </li>
            <li><a class="active" href="#">About</a> </li>
            <li><a class="active" href="#">Property</a> </li>
            <li> <button class="btn">Sign Up!</button> </li>
         </nav>
         <div v-if="isBurger" class="burger_menu">
            <button class="btn">Sign Up!</button>
            <img @click="isBurger = false" class="burger" src="@/assets/burger.svg" alt="">
         </div>
      </div>
      <div>
         <div class="modal" :class="{ 'active': !isBurger }">
            <div class="modal_content">
               <div class="item_logo">
                  <img src="@/assets/logo.svg" alt="">
                  <img @click="isBurger = true" class="close" src="@/assets/close.svg" alt="">
               </div>
               <div class="navbar">
                  <li><a class="active" href="#">Home</a> </li>
                  <li><a  class="active" href="#">About</a> </li>
                  <li><a class="active" href="#">Property</a> </li>
               </div>

            </div>
         </div>
      </div>
   </div>

   <main>
      <div class="container">
         <div class="main_left">
            <img class="main_img" src="@/assets/title.svg" alt="">
            <p class="info">Everything you need about finding your place to live will be here, where it will be easier for
               you. Our
               furniture is made from selected and best quality materials that are suitable for your dream home</p>
            <div class="search">
               <img src="@/assets/locale.svg" alt="">
               <input type="text" placeholder="Search for the location">
               <button><span>Search</span><img src="@/assets/arrow.svg" alt=""></button>
            </div>
            <p class="companu_title">Our Partnership </p>
            <div class="company">
               <img src="@/assets/main1.png" alt="">
               <img src="@/assets/main2.png" alt="">
               <img src="@/assets/main3.png" alt="">
               <img src="@/assets/main4.png" alt="">
            </div>
         </div>
         <div class="main_right">

            <div class="gallery">
               <img class="responsive1" src="@/assets/main_bg.png" alt="">
               <img class="responsive" src="@/assets/bg.jpg" alt="">
            </div>
            <div class="sliderr">
               <swiper :spaceBetween="30"  :centeredSlides="false" :autoplay="{
                  delay: 1500,
                  disableOnInteraction: false,
               }" :breakpoints="{
   '@0.00': {
      slidesPerView: 1,
      spaceBetween: 10,
   },
   '@0.75': {
      slidesPerView: 2.1,
      spaceBetween: 20,
   },

   '@1.50': {
      slidesPerView: 2.4,
      spaceBetween: 50,
   },
}" :modules="modules" class="mySwiper">

                  <swiper-slide>
                     <div class="comment">
                        <img src="@/assets/person1.svg" alt="">
                        <div>
                           <h5>1K+ People</h5>
                           <p>Successfully Getting Home</p>
                        </div>
                     </div>
                  </swiper-slide>
                  <swiper-slide>
                     <div class="comment">
                        <img src="@/assets/person1.svg" alt="">
                        <div>
                           <h5>56 Houses</h5>
                           <p>Sold Monthly</p>
                        </div>
                     </div>
                  </swiper-slide>
                  <swiper-slide>
                     <div class="comment">
                        <img src="@/assets/person1.svg" alt="">
                        <div>
                           <h5>4K+</h5>
                           <p>People Looking</p>
                        </div>
                     </div>
                  </swiper-slide>
                  <swiper-slide>
                     <div class="comment">
                        <img src="@/assets/person1.svg" alt="">
                        <div>
                           <h5>1K+ People</h5>
                           <p>Successfully Getting Home</p>
                        </div>
                     </div>
                  </swiper-slide>
               </swiper>
            </div>
         </div>
      </div>
   </main>
</template>


<style  lang="scss">
.sliderr {
   position: absolute;
   z-index: 999;
   width: 800px;
   bottom: 20px;
   height: 200px;

   .swiper-slide {
      height: 200px;
   }

   .comment {
      display: flex;
      gap: 16px;
      padding: 20px 24px;
      border-radius: 15px;
      background-color: #fff;
      border: 1px;

      h5 {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 600;
         font-size: 16px;
         line-height: 24px;
         color: #1B1C57;
      }

      p {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 200;
         font-size: 12px;
         line-height: 20px;
         color: #68799F;
      }
   }
}

.container {
   max-width: 1390px;
   padding: 0px 30px;
   margin: 0px auto;
   display: flex;
   justify-content: space-between;
   align-items: center;
}

.header {
   position: relative;
   z-index: 9;
   padding-top: 37px;

   .burger {
      display: none;
      width: 24px;
   }

   .close {
      width: 24px;
   }

   .item_logo {
      display: flex;
      justify-content: space-between;
   }

   .modal {
      position: fixed;
      inset: 0;
      z-index: 99999;
      width: 0%;
      height: 100%;
      background-color: rgba(124, 124, 124, 0.8);
      overflow: hidden;
      transition: all 0.4s;

      &.active {
         width: 100%;
         padding: 35px;
      }

      .navbar {
         display: flex;
         flex-direction: column;
         gap: 40px;
         margin-top: 60px;

         li {
            list-style: none;
         }

         a {
            color: #fff;
         }
      }
   }

   img {
      cursor: pointer;
   }

   nav {
      display: flex;
      gap: 55px;
      align-items: center;

      li {
         list-style: none;
      }

      a {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 600;
         font-size: 14px;
         line-height: 18px;
         text-transform: capitalize;
         color: #BDBDBD;

         &.active {
            color: #828282;
         }

      }

   }

   .btn {
      padding: 12px 24px;
      background: #F2994A;
      border-radius: 32px;
      font-family: 'Lexend';
      font-style: normal;
      font-weight: 600;
      font-size: 14px;
      line-height: 22px;
      color: white;
   }

   .burger_menu {
      display: none;
   }

   @media(max-width: 655px) {
      .modal {
         &.active {
            width: 100%;
            padding: 35px;

         }
      }

      .burger_menu {
         display: flex;
         gap: 20px;

         .btn {
            padding: 10px 20px !important;
         }
      }

      nav {
         display: none;
      }

      .burger {
         display: block !important;
      }

   }
}

main {
   .container {
      gap: 30px;
   }

   .main_left {
      width: 45%;
      margin-top: 60px;

      .info {
         margin-top: 24px;
         margin-bottom: 50px;
      }

      .search {
         background: #FFFFFF;
         border: 1px solid #E0E3EB;
         border-radius: 32px;
         display: flex;
         justify-content: space-between;
         height: 56px;
         align-items: center;
         padding-left: 27px;

         input {
            flex-grow: 1;
            border: 0;
            outline: 0;
            padding-left: 10px;
         }

         button {
            padding: 12px 18px;
            background: #F2994A;
            border-radius: 32px;
            font-family: 'Lexend';
            font-style: normal;
            font-weight: 600;
            font-size: 14px;
            line-height: 22px;
            color: white;
            display: flex;
            margin-right: 3px;
         }
      }

      .companu_title {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 400;
         font-size: 16px;
         line-height: 32px;
         margin-top: 80px;
         color: #888B97;
      }

      .company {
         display: flex;
         justify-content: space-between;
         align-items: center;
      }
   }

   .main_right {
      width: 51%;
      overflow: hidden;
      position: absolute;
      top: 0;
      right: 0;
      z-index: 1;

      .gallery {
         display: flex;
         gap: 10px;
         cursor: pointer;
         position: relative;
         z-index: 0;


         img {
            cursor: pointer;
            height: fit-content;
         }

         &:hover {
            justify-content: space-between;

            img {
               width: 50%;
               height: 100vh;
            }
         }
      }
   }

   @media(max-width: 1024px) {
      .main_right {
         width: 45%;
      }

      .main_left {
         width: 53%;
      }
   }

   @media(max-width: 900px) {
      .container {
         flex-direction: column;
      }

      .main_left {
         width: 100%;
         margin-top: 300px;

      }

      .main_right {
         width: 100%;
         top: 0px;
         z-index: -99;
         height: 50%;

         .gallery {
            .responsive1 {
               display: none;
            }
         }

         .sliderr {
            bottom: -30px;
            width: 100%;

            // padding: 30px;
            .comment {
               padding: 12px 15px;
            }
         }
      }

   }

   @media(max-width: 500px) {
      .container {
         padding: 0px 20px;
      }

      .main_left {
         .main_img {
            width: 100%;
         }

         .company {
            flex-wrap: wrap;
            gap: 0px 50px;
         }

         .companu_title {
            margin-top: 40px;
         }

         .search {
            padding-left: 14px;
            height: 49px;

            input {
               width: 110px;
               padding-left: 10px;
            }

            img {
               width: 20px;
               height: 20px;
            }

            button {
               padding: 10px 16px;

               img {
                  height: 20px;
               }
            }
         }

      }
   }
}
</style>
