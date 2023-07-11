<template>
  <v-container class="my-15 text-center">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4" justify="center">
          Contact Us
        </v-subheader>
        <p>Got a question or feedback? Don't hesitate to get in touch with us. Our friendly team is always here to help!</p>
      </v-col>
    </v-row>

    

  <v-row align="center" justify="center" class="ma-12">
    <v-col cols="12" md="8">
      <v-card class="elevation-6">
        <v-card-title class="headline text-center">Get in Touch</v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field label="Name" required></v-text-field>
            <v-text-field label="Email" required></v-text-field>
            <v-textarea label="Message" required></v-textarea>
            <v-btn color="green darken-1" type="submit">Submit</v-btn>
          </v-form>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>


</v-container>
</template>



<script>


export default {
  data() {
    return {
      name: '',
      email: '',
      message: '',
    };
  },
}
</script>


<style scoped>
.v-card__title {
  background-color: #f5f5f5;
  padding: 16px;
}

.v-card__text {
  padding: 16px;
}

.v-input__control {
  border: 1px solid #e5e5e5;
}

.v-btn {
  text-transform: none;
  color: white;
}

.v-btn--flat {
  background-color: transparent;
}

.v-btn--flat:hover {
  background-color: rgba(255, 255, 255, 0.1);
}

.v-btn--icon {
  padding: 6px;
}

.v-divider {
  background-color: white;
}

.red {
  background-color: #f44336;
}

.text-h4 {
  color: #757575;
  font-weight: 800;
  margin-bottom: 16px;
}

.elevation-6 {
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1), 0px 1px 3px rgba(0, 0, 0, 0.08);
}

.elevation-12 {
  box-shadow: 0px 10px 15px rgba(0, 0, 0, 0.1), 0px 4px 6px rgba(0, 0, 0, 0.08);
}
</style>
