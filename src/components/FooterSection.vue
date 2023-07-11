<template>
    <v-footer dark padless>
      <v-card flat tile class="green lighten-1 white--text text-center">
        <v-card-text class="d-flex justify-center">
          <v-btn v-for="icon in icons" :key="icon" class="mx-4 white--text" icon>
            <v-icon size="24px">{{ icon }}</v-icon>
          </v-btn>
        </v-card-text>
  
        <v-card-text class="white--text pt-0">
          Thank you for using Fit Track! We are dedicated to helping you achieve your fitness goals and improve your overall well-being. Please note that our website is for informational purposes only and should not replace medical advice from a healthcare professional. Always consult with your doctor before starting any new exercise or nutrition program. Stay healthy and happy!
        </v-card-text>
  
        <v-divider class="my-4"></v-divider>
  
        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} — <strong>HealthTraq</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </template>
  
  <script>
  export default {
    data: () => ({
      icons: [
        'bx bxl-facebook',
        'bx bxl-twitter',
        'bx bxl-linkedin',
        'bx bxl-youtube',
        'bx bxl-instagram-alt',
      ],
    }),
  };
  </script>
  
  <style scoped>
  .v-footer {
    margin-top: auto;
  }
  
  .v-card {
    box-shadow: none;
  }
  
  .v-divider {
    background-color: white;
  }
  
  .v-card-text {
    font-size: 14px;
    line-height: 1.6;
  }

  .v-btn:hover {
  background-color: rgb(52, 143, 149);
  color: #50C878;
}

  </style>
  
