<script setup>

</script>
<template>
   <div class="container">
      <div class="video_title">
         <h5>Ready to Sell!</h5>
         <h3>Let’s tour and see our house!</h3>
         <p>Houses recommended by our partners that have been curated to become the home of your dreams!</p>
         <h4>House Detail</h4>

         <div class="img_item">
            <div class="img">
               <img src="@/assets/icon1.svg" alt="">
               <p>4 Bedrooms</p>
            </div>
            <div class="img">
               <img src="@/assets/icon2.svg" alt="">
               <p>2 Bathrooms</p>
            </div>
            <div class="img">
               <img src="@/assets/icon3.svg" alt="">
               <p>1 Carport</p>
            </div>
            <div class="img">
               <img src="@/assets/icon4.svg" alt="">
               <p>2 Floors</p>
            </div>
         </div>
         <hr>
         <div class="cal">
            <div class="cal_left">
               <img src="@/assets/vid.svg" alt="">
               <div>
                  <h6>Dianne Russell</h6>
                  <p>Manager Director</p>
               </div>
            </div>
            <button class="cal_right">
               <img src="@/assets/cal.svg" alt="">
               <span>Contact Now</span>
            </button>
         </div>
      </div>
      <div class="video_item">
         <img src="@/assets/svitafor.svg" alt="">
         <!-- <video src="@/assets/video.mp4"></video> -->
         <video width="320" height="240" controls>
            <source src="@/assets/video.mp4" type="video/mp4">
            <!-- <source src="movie.ogg" type="video/ogg"> -->
            Your browser does not support the video tag.
         </video>
      </div>
   </div>
</template>


<style lang="scss" scoped>
.container {
   display: flex;
   gap: 30px;

   .video_title {
      width: 45%;
   }

   h5 {
      font-family: 'Lexend';
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;

      color: #F59E0B;

   }

   h3 {
      font-family: 'Lexend';
      font-style: normal;
      font-weight: 600;
      font-size: 34px;
      line-height: 40px;
      text-transform: capitalize;
      color: #1B1C57;
   }

   p {
      font-family: 'Lexend';
      font-style: normal;
      font-weight: 400;
      font-size: 16px;
      line-height: 28px;
      color: #626687;
      width: 80%;
   }

   h4 {
      font-family: 'Lexend';
      font-style: normal;
      font-weight: 600;
      font-size: 16px;
      line-height: 28px;
      color: #1B1C57;
      margin-top: 16px;
      margin-bottom: 20px;
      opacity: 0.75;
   }

   .img_item {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 30px;

      .img {
         width: 49%;
         display: flex;
         gap: 14px;
         align-items: center;
      }
   }

   hr {
      color: rgb(226, 221, 221);
      border: 1px solid #ccc;
   }

   .cal {
      margin-top: 30px;
      display: flex;
      justify-content: space-between;
      align-items: center;

      .cal_left {
         display: flex;
         gap: 16px;
         width: 70%;

         div {
            h6 {
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
               font-size: 16px;
               line-height: 24px;
               color: #888B97;
               white-space: nowrap;
            }
         }
      }

      .cal_right {
         background: #F2994A;
         border-radius: 32px;
         display: flex;
         gap: 12px;
         padding: 12px 16px;

         span {
            color: white;
            font-family: 'Lexend';
            font-style: normal;
            font-weight: 600;
            font-size: 14px;
            line-height: 22px;
         }
      }
   }

   .video_item {
      width: 55%;
      padding: 20px;
      width: 50%;
      border-radius: 20em;
      border-width: 4px;
      border-style: solid;
      border-image:
         linear-gradient(to bottom,
            rgba(188, 177, 177, 0.53),
            rgba(111, 106, 106, 0)) 1;
      // border-image: linear-gradient(to top, 111.29deg, rgba(255, 255, 255, 0.53) -1.83%, rgba(255, 255, 255, 0) 109.95%);
      box-shadow: 50px 60px 100px rgba(0, 0, 0, 0.05);

      // border: 4px solid;
      video {
         margin-top: 30px;
         width: 100%;
         overflow: hidden;
         border-radius: 10px;
      }
   }

   @media(max-width: 1100px) {
      h3 {
         font-size: 26px;
         margin-top: 6px;
      }

      p {
         width: 100%;
      }

      .img_item {
         margin-bottom: 20px;

         .img {
            width: 46%;
         }
      }

      .cal {
         margin-top: 10px;

         .cal_left {
            width: auto;

            img {
               width: 45px;
               height: 45px;
            }

            div {

               h6 {
                  font-size: 14px;
               }

               p {
                  font-size: 14px;
               }
            }
         }
      }
   }

   @media(max-width: 840px) {
      flex-direction: column;

      .video_title {
         width: 100%;
      }

      .video_item {
         width: 100%;
      }
   }

   @media(max-width: 556px) {

      padding: 0px 20px;

      .cal .cal_left img {
         width: 36px;
         height: 36px;
      }

      .cal .cal_left {
         gap: 10px;

         div {

            p,
            h6 {
               font-size: 12px;
               font-weight: 300;
               line-height: 1.4;
            }


         }
      }

      h3 {
         font-size: 22px;
      }

      p {
         font-size: 14px;
         font-weight: 300;
         line-height: 1.5;
      }

      .cal .cal_right {
         padding: 8px 10px;
         gap: 4px;

         img {
            width: 20px;
            height: 20px;
         }

         span {
            font-weight: 300;
         }
      }
   }
}</style>