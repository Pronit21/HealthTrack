<template>
  <v-container>
    <v-row align="center">
      <v-col cols="12" md="6" class="pr-md-5">
  <img src="./../assets/sports.avif" alt="" class="ml-8" style="max-width: 100%;">
</v-col>
      <v-col cols="12" md="6" class="pl-md-5 about-text-col">
        <button><v-subheader class="text-h5">About Us</v-subheader></button>
<br>
        <p>Welcome to HealthTraq, your personal health and wellness tracker. We believe that taking control of your health starts with understanding it. That's why we've created an easy-to-use platform that allows you to track your fitness, nutrition, and other health metrics all in one place.</p>
        

        <v-list>
          <v-list-item>
            <v-icon color="success">mdi-check-all</v-icon>
            <v-list-item-subtitle>Our mission is to empower you to make informed decisions about your health by providing you with accurate and up-to-date information.</v-list-item-subtitle>
          </v-list-item>
          <v-list-item>
            <v-icon color="success">mdi-check-all</v-icon>
            <v-list-item-subtitle> We're dedicated to helping you reach your goals and live a healthier, happier life.</v-list-item-subtitle>
          </v-list-item>
          <v-list-item>
            <v-icon color="success">mdi-check-all</v-icon>
            <v-list-item-subtitle>Start tracking your health today and see the difference it can make!</v-list-item-subtitle>
          </v-list-item>
        </v-list>

      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'AboutUs',
}
</script>


<style scoped>
.about-text-col {
  padding-left: 7rem; /* adjust the padding value as needed */
}

button {
    cursor: pointer;
    position: relative;
    padding: 22px 46px;
    font-size: 20px;
    text-transform: uppercase;
    color: #ffffff;
    background: rgba(255, 255, 255, .1);
    border: 3px solid rgba(255, 255, 255, .2);
    border-radius: 18px;
    transition: .4s;
}

button:hover {
    z-index: 1;
    border-color: transparent;
    background: linear-gradient(
        90deg,
        #f9d923,
        #00a19d,
        #0c87b7,
        #cb49ff,
        #ff6666,
        #f9d923
    );
    background-size: 300%;
    box-shadow: 0 0 15px rgb(2, 4, 24);
    animation: glow 12s linear forwards;
}

@keyframes glow {

    from {
        background-position: 0%;
    }

    to {
        background-position: 400%;
    }

}

button::before {
    content: '';
    position: absolute;
    top: -1px;
    right: -1px;
    bottom: -1px;
    left: -1px;
    background: inherit;
    filter: blur(36px);
    opacity: 0;
    transition: .4s ease-out;
}

button:hover::before {
    opacity: 1; 
    z-index: -1;
}


</style>
