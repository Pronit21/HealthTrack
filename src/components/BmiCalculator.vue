<template>
    <v-container>
      <v-card>
        <v-card-title class="headline">BMI Calculator</v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field v-model="height" type="number" label="Height (cm)"></v-text-field>
            <v-text-field v-model="weight" type="number" label="Weight (kg)"></v-text-field>
            <v-btn color="green darken-1" @click="calculateBMI">Calculate BMI</v-btn>
          </v-form>
          <v-divider></v-divider>
          <v-alert v-if="bmi" :value="true" :color="getBMIColor(bmi)" dense outlined>
            <p>Your BMI is {{ bmi.toFixed(1) }}</p>
            <p>{{ getBMICategory(bmi) }}</p>
          </v-alert>
        </v-card-text>
      </v-card>
    </v-container>
  </template>
  
  <script>
  export default {
    data() {
      return {
        height: null,
        weight: null,
        bmi: null,
      };
    },
    methods: {
      calculateBMI() {
        this.bmi = this.weight / ((this.height / 100) ** 2);
      },
      getBMICategory(bmi) {
        if (bmi < 18.5) {
          return "Underweight";
        } else if (bmi < 25) {
          return "Normal weight";
        } else if (bmi < 30) {
          return "Overweight";
        } else {
          return "Obese";
        }
      },
      getBMIColor(bmi) {
        if (bmi < 18.5) {
          return "warning";
        } else if (bmi < 25) {
          return "success";
        } else if (bmi < 30) {
          return "orange darken-2";
        } else {
          return "red darken-2";
        }
      },
    },
  };
  </script>
  