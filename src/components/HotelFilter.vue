      
<script setup>
import { ref } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';

import 'swiper/css/pagination';
import 'swiper/css/navigation';

// import './style.css';

import { Autoplay, Pagination, Navigation } from 'swiper';


const modules = [Autoplay, Pagination, Navigation]
const isHouse = ref(true)
const isVilla = ref(false)
const isApartment = ref(false)
function handleBtn(item) {
   isHouse.value = false;
   isVilla.value = false;
   isApartment.value = false;
   if (item == 'house') {
      isHouse.value = true;
   }
   else if (item == 'villa') {
      isVilla.value = true;
   }
   else {
      isApartment.value = true;

   }
}
</script>
<template>
   <div class="hotel">
      <div class="container">
         <div>
            <p style="color:#F2994A">Our Recommendation</p>
            <h2>Featured House</h2>
         </div>
         <div class="filter_btn">
            <button @click="handleBtn('house')" :class="{ 'active': isHouse }">
               <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path
                     d="M21 10.8319V19.5C20.9998 19.7719 20.9262 20.0386 20.7868 20.272C20.6475 20.5054 20.4476 20.6968 20.2084 20.8259C19.9916 20.9432 19.7485 21.0031 19.5021 20.9999H14.9967C14.7978 20.9999 14.607 20.9209 14.4664 20.7803C14.3257 20.6396 14.2467 20.4488 14.2467 20.2499V15.7493C14.2467 15.5504 14.1677 15.3596 14.0271 15.2189C13.8864 15.0783 13.6956 14.9993 13.4967 14.9993H10.4967C10.2978 14.9993 10.107 15.0783 9.9664 15.2189C9.82574 15.3596 9.74673 15.5504 9.74673 15.7493V20.2499C9.74673 20.4488 9.66771 20.6396 9.52706 20.7803C9.3864 20.9209 9.19564 20.9999 8.99673 20.9999H4.5002C4.28754 21.0005 4.07723 20.9556 3.88335 20.8682C3.68948 20.7808 3.51651 20.653 3.37604 20.4934C3.12946 20.2082 2.99571 19.8427 3.00001 19.4657V10.8318C3.00017 10.6228 3.04392 10.4162 3.12846 10.225C3.21299 10.0339 3.33646 9.86251 3.49098 9.7218L10.9903 2.90308C11.2658 2.65075 11.6258 2.51078 11.9994 2.51074C12.3729 2.51071 12.733 2.65062 13.0085 2.90289L20.5091 9.72189C20.6636 9.86263 20.787 10.034 20.8716 10.2252C20.9561 10.4163 20.9998 10.6229 21 10.8319Z"
                     fill="#F2994A" />
               </svg>
               <span>House</span>
            </button>
            <button @click="handleBtn('villa')" :class="{ 'active': isVilla }"><svg width="24" height="24"
                  viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path
                     d="M7 20.9999H4C3.45 20.9999 3 20.5499 3 19.9999V8.68994C3 8.26994 3.25 7.89994 3.64 7.74994L14.64 3.51994C14.7921 3.46126 14.9561 3.44064 15.118 3.45986C15.2798 3.47909 15.4345 3.53758 15.5686 3.63025C15.7027 3.72292 15.8121 3.84696 15.8873 3.99156C15.9624 4.13617 16.0012 4.29696 16 4.45994V9.99994H8C7.45 9.99994 7 10.4499 7 10.9999V20.9999ZM17 11.9999H10C9.45 11.9999 9 12.4499 9 12.9999V19.9999C9 20.5499 9.45 20.9999 10 20.9999H14V16.9999C14 16.4499 14.45 15.9999 15 15.9999C15.55 15.9999 16 16.4499 16 16.9999V20.9999H20C20.55 20.9999 21 20.5499 21 19.9999V11.9999C21 10.8999 20.1 9.99994 19 9.99994C17.9 9.99994 17 10.8999 17 11.9999Z"
                     fill="#888B97" />
               </svg>
               <span>Villa</span>

            </button>
            <button @click="handleBtn('apartment')" :class="{ 'active': isApartment }">
               <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path
                     d="M17 11V5C17 3.9 16.1 3 15 3H9C7.9 3 7 3.9 7 5V7H5C3.9 7 3 7.9 3 9V19C3 20.1 3.9 21 5 21H11V17H13V21H19C20.1 21 21 20.1 21 19V13C21 11.9 20.1 11 19 11H17ZM7 19H5V17H7V19ZM7 15H5V13H7V15ZM7 11H5V9H7V11ZM11 15H9V13H11V15ZM11 11H9V9H11V11ZM11 7H9V5H11V7ZM15 15H13V13H15V15ZM15 11H13V9H15V11ZM15 7H13V5H15V7ZM19 19H17V17H19V19ZM19 15H17V13H19V15Z"
                     fill="#888B97" />
               </svg>
               <span>Apartment</span>
            </button>
         </div>
      </div>
      <div class="filter_card">
         <swiper style="padding-bottom: 40px;" v-if="isHouse" :spaceBetween="30" :slides-per-view="3.8"
            :centeredSlides="false" :autoplay="{
               delay: 150000,
               disableOnInteraction: false,
            }" :modules="modules" :breakpoints="{
   '@0.05': {
      slidesPerView: 1,
      spaceBetween: 10,
   },
   '@0.75': {
      slidesPerView: 1.8,
      spaceBetween: 10,
   },
   '@1.00': {
      slidesPerView: 2.1,
      spaceBetween: 10,
   },

   '@1.50': {
      slidesPerView: 3.8,
      spaceBetween: 40,
   }
}" class="mySwiper">
            <swiper-slide v-for="item in 9" :key="item">
               <div class="card">
                  <div class="card_img">
                     <img src="@/assets/card1.png" alt="">
                     <button>
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                           <path
                              d="M21 10.8319V19.5C20.9998 19.7719 20.9262 20.0386 20.7868 20.272C20.6475 20.5054 20.4476 20.6968 20.2084 20.8259C19.9916 20.9432 19.7485 21.0031 19.5021 20.9999H14.9967C14.7978 20.9999 14.607 20.9209 14.4664 20.7803C14.3257 20.6396 14.2467 20.4488 14.2467 20.2499V15.7493C14.2467 15.5504 14.1677 15.3596 14.0271 15.2189C13.8864 15.0783 13.6956 14.9993 13.4967 14.9993H10.4967C10.2978 14.9993 10.107 15.0783 9.9664 15.2189C9.82574 15.3596 9.74673 15.5504 9.74673 15.7493V20.2499C9.74673 20.4488 9.66771 20.6396 9.52706 20.7803C9.3864 20.9209 9.19564 20.9999 8.99673 20.9999H4.5002C4.28754 21.0005 4.07723 20.9556 3.88335 20.8682C3.68948 20.7808 3.51651 20.653 3.37604 20.4934C3.12946 20.2082 2.99571 19.8427 3.00001 19.4657V10.8318C3.00017 10.6228 3.04392 10.4162 3.12846 10.225C3.21299 10.0339 3.33646 9.86251 3.49098 9.7218L10.9903 2.90308C11.2658 2.65075 11.6258 2.51078 11.9994 2.51074C12.3729 2.51071 12.733 2.65062 13.0085 2.90289L20.5091 9.72189C20.6636 9.86263 20.787 10.034 20.8716 10.2252C20.9561 10.4163 20.9998 10.6229 21 10.8319Z"
                              fill="#1D4ED8" />
                        </svg>
                        <span>New house</span>
                     </button>
                  </div>
                  <div class="card_title">
                     <h3>Woodlandside</h3>
                     <p>$ 20.000.000</p>
                     <div class="box">
                        <img src="@/assets/box1.png" alt="">
                        <div>
                           <h5>Robert Fox</h5>
                           <span>Dr. San Jose, South Dakota</span>
                        </div>
                     </div>
                  </div>
               </div>

            </swiper-slide>
         </swiper>
         <swiper v-else-if="isVilla" :spaceBetween="30" :slides-per-view="3.8" :centeredSlides="false" :autoplay="{
            delay: 1500,
            disableOnInteraction: false,

         }" :breakpoints="{
   '@0.05': {
      slidesPerView: 1,
      spaceBetween: 10,
   },
   '@0.75': {
      slidesPerView: 1.8,
      spaceBetween: 10,
   },
   '@1.00': {
      slidesPerView: 2.1,
      spaceBetween: 10,
   },

   '@1.50': {
      slidesPerView: 3.8,
      spaceBetween: 40,
   }
}" :modules="modules" class="mySwiper">
            <swiper-slide v-for="item in 9" :key="item">
               <div class="card">
                  <div class="card_img">
                     <img src="@/assets/card2.png" alt="">
                     <button style="background: #D1FAE5;">
                        <img style="width: 24px; height: 24px;" src="@/assets/wallet.svg" alt="">

                        <span style="color: #047857"> Best Deals </span>
                     </button>
                  </div>
                  <div class="card_title">
                     <h3>Woodlandside</h3>
                     <p>$ 20.000.000</p>
                     <div class="box">
                        <img src="@/assets/box1.png" alt="">
                        <div>
                           <h5>Robert Fox</h5>
                           <span>Dr. San Jose, South Dakota</span>
                        </div>
                     </div>
                  </div>
               </div>

            </swiper-slide>
         </swiper>
         <swiper v-else-if="isApartment" :spaceBetween="30" :slides-per-view="3.8" :centeredSlides="false" :autoplay="{
            delay: 1500,
            disableOnInteraction: false,
         }" :breakpoints="{
   '@0.05': {
      slidesPerView: 1,
      spaceBetween: 10,
   },
   '@0.75': {
      slidesPerView: 1.8,
      spaceBetween: 10,
   },
   '@1.00': {
      slidesPerView: 2.1,
      spaceBetween: 10,
   },

   '@1.50': {
      slidesPerView: 3.8,
      spaceBetween: 40,
   }
}" :modules="modules" class="mySwiper">
            <swiper-slide v-for="item in 9" :key="item">
               <div class="card">
                  <div class="card_img">
                     <img src="@/assets/card3.png" alt="">
                     <button style="background: #FEE2E2;">
                        <img style="width: 24px; height: 24px;" src="@/assets/fire.svg" alt="">
                        <span style="color:#EF4444">Popular</span>
                     </button>
                  </div>
                  <div class="card_title">
                     <h3>Woodlandside</h3>
                     <p>$ 20.000.000</p>
                     <div class="box">
                        <img src="@/assets/box1.png" alt="">
                        <div>
                           <h5>Robert Fox</h5>
                           <span>Dr. San Jose, South Dakota</span>
                        </div>
                     </div>
                  </div>
               </div>

            </swiper-slide>
         </swiper>
      </div>
   </div>
</template>

<style lang="scss" >
.hotel {
   margin-top: 220px;
   margin-bottom: 40px;

   .filter_btn {
      display: flex;
      gap: 35px;

      button {
         display: flex;
         align-items: center;
         gap: 6px;
         border-radius: 32px;
         border: 1px solid #888B97;
         padding: 12px 24px;

         span {
            font-family: 'Lexend';
            font-style: normal;
            font-weight: 500;
            font-size: 18px;
            line-height: 28px;
            color: #888B97;
         }

         svg path {
            fill: #888B97;
         }

         &.active {
            border: 1px solid #D1FAE5;
            background: #D1FAE5;

            svg path {
               fill: #F2994A;
            }

            span {
               color: #F2994A;
            }
         }
      }
   }

   .filter_card {
      margin-top: 50px;

      .card {

         .card_img {
            position: relative;
            margin-bottom: 18px;

            img {
               width: 100%;
               height: 320px;
            }

            button {
               border-radius: 11px;
               background: #DBEAFE;
               border-radius: 32px;
               position: absolute;
               padding: 8px 18px;
               bottom: 30px;
               left: 20px;
               display: flex;
               align-items: center;
               gap: 8px;

               span {
                  font-family: 'Lexend';
                  font-style: normal;
                  font-weight: 500;
                  font-size: 14px;
                  line-height: 18px;
                  text-transform: capitalize;
                  color: #1D4ED8;
               }
            }
         }
      }

      .card_title {
         .box {
            display: flex;
            gap: 16px;
            margin-top: 21px;

            h5 {
               font-family: 'Lexend';
               font-style: normal;
               font-weight: 500;
               font-size: 18px;
               line-height: 24px;
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
      }
   }

   @media(max-width:890px) {
      .filter_btn {
         gap: 20px;

         button {
            padding: 8px 18px;

            span {
               font-size: 16px;
            }

            svg {
               width: 20px;
               height: 20px;
            }
         }
      }
   }

   @media(max-width:690px) {
      margin-top: 40px;

      .container {
         flex-direction: column;
         justify-content: center;
         align-items: center;
         gap: 40px;
      }

      .filter_card {
         padding: 0px 20px;

         .card_title .box span {
            font-size: 14px;
         }

         .card .card_img button {
            padding: 6px 14px;

            img {
               width: 20px;
               height: 20px;
            }
         }
      }

      .filter_btn {
         gap: 12px;

         button {
            padding: 4px 10px;
            gap: 4px;

            span {
               font-size: 14px;
               font-weight: normal;
            }
         }

      }
   }
}
</style>