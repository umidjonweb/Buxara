<template>
   <div class="footer">
      <div class="container">
         <div class="footer_left">
            <img src="@/assets/logo1.png" alt="">
            <p>We provide information about properties such as houses, villas and apartments to help people find their
               dream home</p>
            <h3>Subscribe to our newsletter!</h3>
            <div class="input">
               <img src="@/assets/email.svg" alt="">
               <input type="text" placeholder="Your email here">
               <el-button plain @click="open1">Subsribe Now</el-button>
            </div>
         </div>
         <div class="footer_right">
            <div class="link">
               <ul>
                  <li>
                     <h3>Property</h3>
                  </li>
                  <li><a href="!#">House</a></li>
                  <li><a href="!#">Apartment</a></li>
                  <li><a href="!#">Villa</a></li>
               </ul>
               <ul>
                  <li>
                     <h3>Article</h3>
                  </li>
                  <li><a href="!#">New Article</a></li>
                  <li><a href="!#">Popular Article</a></li>
                  <li><a href="!#">Most Read</a></li>
                  <li><a href="!#">Tips & Tricks</a></li>
               </ul>
               <ul>
                  <li>
                     <h3>Contact</h3>
                  </li>
                  <li><a href="!#">Medan, South Sumatera</a></li>
                  <li><a href="!#">(62) 81312120001</a></li>
                  <li><a href="!#">halo@homedesk.com</a></li>
               </ul>
            </div>

         </div>
      </div>
   </div>
</template>

<script setup>
import { ElNotification, ElButton } from 'element-plus'
const open1 = () => {
   ElNotification({
      title: 'Success',
      message: 'Emailga xat ketdi',
      type: 'success',
   })
}

</script>

<style lang="scss">
   
      .el-notification {
         height: 90px!important;
      }
.footer {
   margin-top: 100px;

   .container {
      display: flex;
      justify-content: space-between;

      .footer_left {
         width: 40%;
         padding-right: 70px;

         p {
            font-family: 'Lexend';
            font-style: normal;
            font-weight: 400;
            font-size: 14px;
            line-height: 20px;
            color: #626687;

            opacity: 0.75;
            margin-bottom: 15px;
            margin-top: 8px;
         }

         h3 {
            font-family: 'Lexend';
            font-style: normal;
            font-weight: 500;
            font-size: 14px;
            line-height: 18px;
            letter-spacing: -0.3px;
            margin-top: 10px;
            margin-bottom: 5px;
            color: #626687;
            opacity: 0.6;
         }

         .input {
            margin-top: 16px;
            display: flex;
            background: #FFFFFF;
            box-shadow: 0px 9px 32px rgba(89, 92, 219, 0.08);
            border-radius: 32px;
            padding: 4px 4px 4px 24px;

            input {
               border: 0;
               outline: 0;
               flex-grow: 1;
               font-family: 'Lexend';
               font-style: normal;
               font-weight: 500;
               font-size: 14px;
               line-height: 22px;
               color: #888B97;
               margin-left: 20px;
            }

            button {
               padding: 12px 16px;
               background: #F2994A;
               border-radius: 32px;
               font-family: 'Lexend';
               font-style: normal;
               font-weight: 600;
               font-size: 14px;
               line-height: 22px;
               color: #FFFFFF;
            }
         }
      }

      .footer_right {
         padding-left: 50px;
         width: 60%;

         .link {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;

            ul {
               li {
                  list-style: none;
                  margin-top: 18px;

                  a {
                     font-family: 'Lexend';
                     font-style: normal;
                     font-weight: 400;
                     font-size: 14px;
                     line-height: 18px;
                     text-transform: capitalize;
                     color: #888B97;
                  }

                  h3 {
                     font-family: 'Lexend';
                     font-style: normal;
                     font-weight: 600;
                     font-size: 18px;
                     line-height: 22px;
                     text-transform: capitalize;
                     color: #0E1735;
                  }
               }
            }
         }
      }
   }

   @media(max-width: 994px) {
      .container {
         .footer_left {
            width: 45%;
            padding-right: 20px;
         }

         .footer_right {
            width: 53%;
            padding-left: 0;
         }
      }

   }

   @media(max-width: 924px) {
      .container {
         flex-direction: column;

         .footer_left {
            width: 100%;
            padding-right: 0px;
         }

         .footer_right {
            width: 100%;
            padding-left: 0;
         }
      }

   }

   @media(max-width: 556px) {
      margin-top: 50px;

      .container {
         padding: 0px 20px;

         .footer_left .input {
            padding: 2px 2px 2px 8px;

            input {
               margin-left: 12px;
               width: 150px;
            }

            button {
               white-space: nowrap;
               font-size: 12px;
               padding: 9px 13px;
            }
         }

         .footer_right .link {
            flex-wrap: wrap;
         }

         ul {
            padding: 0;
            width: 45%;
         }

      }
   }
}
</style>