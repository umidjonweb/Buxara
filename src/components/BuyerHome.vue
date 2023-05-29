
<script setup>
import { ref } from 'vue';

const isPhoto = ref(true)

</script>
<template>
   <div class="container">
      <div class="line">
         <img class="line2" src="@/assets/line.svg" alt="">
      </div>
      <h5>See tips and trick from our partnership</h5>
      <h2>Find out more about selling and buying homes</h2>
      <div class="buyer">
         <div class="buyer_left">
            <div class="box">
               <img class="photo" @click="isPhoto = true" src="@/assets/buyer1.png" alt="">
               <div class="box_title">
                  <div class="subtitle">
                     <img src="@/assets/vid.svg" alt="">
                     <p>Dianne Russell</p>
                  </div>
                  <h4>The things we need to check when we want to buy a house</h4>
                  <div class="time">
                     <img src="@/assets/time.svg" alt="">
                     <p>4 min read | 25 Apr 2021</p>
                  </div>
               </div>
            </div>
            <div class="box">
               <img class="photo" @click="isPhoto = false" src="@/assets/buyer2.png" alt="">
               <div class="box_title">
                  <div class="subtitle">
                     <img src="@/assets/vid.svg" alt="">
                     <p>Courtney Henry</p>
                  </div>
                  <h4>7 Ways to distinguish the quality of the house we want to buy</h4>
                  <div class="time">
                     <img src="@/assets/time.svg" alt="">
                     <p>4 min read | 25 Apr 2021</p>
                  </div>
               </div>
            </div>
         </div>
         <div class="buyer_right">
            <img v-if="isPhoto" class="gallery" src="@/assets/item1.png" alt="">
            <img v-else class="gallery" src="@/assets/buyer2.png" alt="">
            <div class="cards">
               <div class="cards_box">
                  <img src="@/assets/vid.svg" alt="">
                  <p v-if="isPhoto">Cameron Williamson</p>
                  <p v-else>Courtney Henry</p>
               </div>
               <h3 v-if="isPhoto">12 Things to know before buying a house</h3>
               <h3 v-else>7 Ways to distinguish the quality of the house we want to buy</h3>
               <div class="time">
                  <img src="@/assets/time1.svg" alt="">
                  <p>8 min read | 25 Apr 2021</p>
               </div>
            </div>
         </div>
      </div>

   </div>
</template>

<style lang="scss" scoped>
.container {
   display: block;
   margin-top: 100px;

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

   .buyer {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 70px;

      .buyer_left {
         display: flex;
         flex-direction: column;
         gap: 30px;

         .box {
            display: flex;
            justify-content: space-between;
            align-items: center;

            .photo {
               cursor: pointer;
            }
         }

         .box_title {
            padding-left: 32px;

            .subtitle {
               display: flex;
               gap: 16px;
               align-items: center;

               p {
                  font-family: 'Lexend';
                  font-style: normal;
                  font-weight: 400;
                  font-size: 14px;
                  line-height: 22px;
                  color: #3C4563;
               }

               img {
                  width: 32px;
                  height: 32px;
               }
            }

            h4 {
               font-family: 'Lexend';
               font-style: normal;
               font-weight: 500;
               font-size: 18px;
               line-height: 32px;
               text-transform: capitalize;
               color: #1B1C57;
               margin-top: 12px;
               margin-bottom: 9px;
            }
         }

         .time {
            display: flex;
            align-items: center;
            gap: 14px;

            p {

               font-family: 'Lexend';
               font-style: normal;
               font-weight: 400;
               font-size: 14px;
               line-height: 24px;
               color: #888B97;

            }
         }
      }

      .buyer_right {
         position: relative;
         border-radius: 16px;
         background: linear-gradient(180deg, rgba(0, 0, 0, 0) 10%, rgba(0, 0, 0, 0.78) 100%);

         .gallery {
            position: absolute;
            z-index: -1;
            width: 100%;
            height: 100%;
         }

         .cards {
            position: absolute;
            bottom: 20px;
            left: 25px;

            .cards_box {
               display: flex;
               align-items: center;
               gap: 16px;

               img {
                  width: 32px;
                  height: 32px;
               }

               p {
                  font-family: 'Lexend';
                  font-style: normal;
                  font-weight: 700;
                  font-size: 14px;
                  line-height: 22px;
                  color: #F2F2F2;
               }
            }

            h3 {
               font-family: 'Lexend';
               font-style: normal;
               font-weight: 500;
               font-size: 24px;
               line-height: 32px;
               text-transform: capitalize;
               color: #F2F2F2;
               margin-top: 8px;
               margin-bottom: 10px;
            }

            .time {
               display: flex;
               gap: 10px;

               p {
                  font-family: 'Lexend';
                  font-style: normal;
                  font-weight: 400;
                  font-size: 14px;
                  line-height: 24px;
                  color: #F2F2F2;
               }
            }
         }
      }
   }

   @media(max-width: 1024px) {
      .buyer {
         gap: 30px;

         .buyer_left {
            gap: 20px;

            .box_title {
               padding-left: 14px;

               h4 {
                  line-height: 1.4;
                  font-size: 15px;
                  font-weight: 400;
               }
            }
         }

         .buyer_right .cards {
            left: 15px;

            h3 {
               font-size: 20px;
            }
         }
      }
   }

   @media(max-width: 924px) {
      .buyer {
         grid-template-columns: repeat(1, minmax(0, 1fr));

         .buyer_right {
            height: 350px;
         }

         .buyer_left .box {
            gap: 30px;
            justify-content: start;
         }
      }
   }

   @media(max-width: 556px) {
      padding: 0px 20px !important;

      .buyer .buyer_left .box .photo {
         width: 140px;
      }

      .buyer .buyer_left .box_title .subtitle img {
         width: 24px;
         height: 24px;
      }

      .buyer .buyer_right .cards .cards_box {
         gap: 10px;
      }

      .buyer .buyer_right {
         height: 250px;
      }

      .buyer .buyer_right .cards h3 {
         font-size: 15px;
         line-height: 1.3;
         font-weight: 300;
      }

      h2 {
         margin-bottom: 30px;
         font-size: 20px;
         line-height: 1.4;
      }

      .buyer .buyer_left .box {
         gap: 10px;
      }

      .buyer .buyer_left .box_title {
         padding-left: 0;

         h4 {
            font-size: 11px;
            margin-top: 2px;
            margin-bottom: 4px;
         }
      }
      .buyer .buyer_left .box_title .subtitle{
       gap: 10px;
      }

      .buyer .buyer_left .time {
         gap: 4px;

         img {
            width: 20px;
            height: 20px;
         }

         p {
            font-size: 11px;
         }
      }
   }
}
</style>