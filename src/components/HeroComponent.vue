<template>
  <v-container class="hero fill-height" fluid>
    <v-row justify="center" align="center">
      <v-col lg="6" md="8" sm="10" xs="12" class="text-center">
        <h2 class="intro-text mb-4 display-2 font-weight-bold">A YOU FIRST APPROACH TO WELLNESS</h2>
        <p class="description mb-6 body-1 font-weight-bold" ></p>
        <v-btn color="red accent-2" class="white--text mr-4" rounded @click="navigateToLogin()">Dashboard</v-btn>
        <v-btn color="purple accent-3" class="white--text" rounded>Watch Video</v-btn>
      </v-col>
      <v-col lg="6" class="d-flex align-center">
       
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
  name: "HeroComponent",
  methods: {
    gotoNewPage() {
      this.$router.push({ path: "" });
    },
    navigateToLogin() {
      window.location.href = "http://localhost:8082/";
    },
  },
};
</script>

<style scoped>

.hero {
  background: none;
  color: #fff;
  padding: 50px;
  margin-top: -790px;
  height: 100vh;
  width: 100%;
  position: relative;
  z-index: 1;
}

.hero:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-image: url('@/assets/vitalii-pavlyshynets-kcRFW-Hje8Y-unsplash.jpg');
  background-size: cover;
  background-position: center;
  opacity: 0.8;
  z-index: -1;
}

 
  .fill-height {
    /* add min-height */
    min-height: 100vh;
  }

  h2.intro-text {
    font-size: 60px;
    text-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
    color: rgb(240, 246, 241);
    border: 35px;
    border-color:blue; }

  p.description {
    font-size: 22px;
    max-width: 80%;
    margin: 0 auto;
    color: rgb(132, 170, 37);
  }

  .v-btn {
    font-size: 18px;
    font-weight: bold;
    padding: 10px 20px;
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-top: 40px;
  }

  .hero img {
    max-height: 600px;
    max-width: 100%;
    object-fit: contain;
  }

  @media (max-width: 1024px) {
    h2.intro-text {
      font-size: 50px;
    }

    p.description {
      font-size: 20px;
      max-width: 100%;
      margin: 0 auto;
    }
  }

  @media (max-width: 768px) {
    h2.intro-text {
      font-size: 40px;
    }

    p.description {
      font-size: 18px;
      max-width: 100%;
      margin: 0 auto;
    }

    .v-btn {
      font-size: 16px;
      padding: 8px 16px;
    }
  }

  @media (max-width: 480px) {
    h2.intro-text {
      font-size: 32px;
    }

    p.description {
      font-size: 16px;
      max-width: 100%;
      margin: 0 auto;
    }

    .v-btn {
      font-size: 14px;
      padding: 6px 12px;
      margin-top: 20px;
    }
  }
</style>
