<template>
   <router-view />
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800&family=Lexend:wght@100;200;300;400;500;600;700;800;900&family=Manrope:wght@200;300;400;500;600;700;800&family=Noto+Sans:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,400&family=Nunito+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;0,900;1,400;1,600;1,700;1,800&family=Open+Sans:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,300&family=Padauk:wght@400;700&family=Poppins:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,400;1,600&family=Red+Hat+Display:wght@300;400;500;600;700;800;900&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,300;1,500&family=Rubik:ital,wght@0,300;0,400;0,500;0,600;1,300&family=Space+Grotesk:wght@300;400;500;600;700&family=Ubuntu:ital,wght@0,700;1,300;1,400&display=swap');

* {
   margin: 0;
   bottom: 0;
   box-sizing: border-box;
}

.container {
   max-width: 1390px;
   padding: 0px 30px;
   margin: 0px auto;

   @media(max-width:556px) {
      padding: 0px 20px;

   }
}

body {
   font-family: Lexend;
}

a {
   text-decoration: none;
   cursor: pointer;
}

button {
   cursor: pointer;
   background-color: transparent;
   border: 0;
   outline: 0;
}</style>
