<script setup>

</script>
<template>
   <div class="benefit">
      <div class="container">
         <div class="benefit_left">
            <h4 class="h4">Benefit</h4>
            <h2>Benefit You Get When Using Our Services</h2>
            <h1>600+</h1>
            <p>Home Furniture throughout Indonesia</p>
            <h1>135+</h1>
            <p>Staff ready to help you</p>
         </div>
         <div class="benefit_right">
            <div class="box">
               <img src="@/assets/check1.svg" alt="">
               <div>
                  <h4>Best Quality</h4>
                  <p>All of our funiture uses the best materials and choices for our customers.</p>
               </div>
            </div>
            <div class="box">
               <img src="@/assets/check2.svg" alt="">
               <div>
                  <h4>Free Shipping</h4>
                  <p>All of our funiture uses the best materials and choices for our customers.</p>
               </div>
            </div>
            <div class="box">
               <img src="@/assets/check3.svg" alt="">
               <div>
                  <h4>Space Customization</h4>
                  <p>All of our funiture uses the best materials and choices for our customers.</p>
               </div>
            </div>
         </div>

      </div>
   </div>
</template>


<style lang="scss" scoped>
.benefit {
   margin: 70px 0px;

   .container {}

   .benefit_left {
      h4 {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 500;
         font-size: 18px;
         line-height: 22px;
         color: #F59E0B;
      }

      h2 {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 600;
         font-size: 32px;
         line-height: 40px;
         color: #1B1C57;
         width: 70%;
      }

      h1 {
         margin-top: 50px;
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 500;
         font-size: 80px;
         line-height: 90px;
         letter-spacing: 0.888889px;
         color: #1EA59A;

      }

      p {
         font-family: 'Lexend';
         font-style: normal;
         font-weight: 300;
         font-size: 15px;
         line-height: 25px;

         letter-spacing: 0.346154px;

         color: #404852;
      }
   }

   .benefit_right {

      background: #F6FAFA;
      box-shadow: 12px 16px 25px rgba(0, 0, 0, 0.04);
      padding: 60px 90px;
      border-radius: 20px;
      display: flex;
      flex-direction: column;
      gap: 50px;

      .box {
         display: flex;
         gap: 30px;
         align-items: flex-start;

         div {

            h4 {
               font-style: normal;
               font-weight: 600;
               font-size: 24px;
               line-height: 25px;
               letter-spacing: 0.352941px;
               color: #000B70;
            }

            p {
               font-family: 'Lexend';
               font-style: normal;
               font-weight: 300;
               font-size: 18px;
               line-height: 28px;
               color: #B1B6CA;
            }
         }
      }
   }

   @media(max-width:1100px) {
      .benefit_left {
         h2 {

            width: 100%;
            font-size: 30px;
         }

         h1 {
            margin-top: 30px;
            font-size: 70px;
         }
      }

      .benefit_right {
         padding: 20px 30px;
      }
   }

   @media(max-width: 768px) {
      .container {
         flex-direction: column;
         gap: 40px;

         .h4 {
            text-align: center;
         }

         .benefit_left h2 {
            font-size: 24px;
            margin-top: 8px;
         }
      }

      .benefit_left {
         h2 {

            width: 100%;
            font-size: 30px;
         }

         h1 {
            margin-top: 30px;
            font-size: 70px;
         }
      }

      .benefit_right {
         padding: 20px 30px;
      }
   }

   @media(max-width: 556px) {
      margin-top: 20px;

      .container {
         padding: 0px 20px;

         .benefit_left {
            h2 {
               font-size: 18px;
               line-height: 1.5;
            }
            h1{
               margin-top: 10px;
               line-height: 76px;
            }
         }

         .benefit_right {
            padding: 10px 15px;

            .box {
               gap: 20px;

               img {
                  width: 40px;
                  height: 40px;
               }

               h1 {
                  margin-top: 16px;
                  font-size: 56px;
                  line-height: 60px;
               }

               h4 {
                  font-size: 18px;
               }

               p {
                  font-size: 14px;
                  font-weight: 200;
                  line-height: 1.3;
               }
            }


         }



      }
   }
}</style>