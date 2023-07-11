<template>
  <div class="fitness-calculator" :style="{ background: 'linear-gradient(to bottom right, #dae3e4, #4caf50)' }">
    <v-container>
      <v-card class="elevation-4">
        <v-card-title class="headline">Fitness Calculator</v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field v-model="age" type="number" label="Age"></v-text-field>
            <v-select v-model="gender" :items="genders" label="Gender"></v-select>
            <v-text-field v-model="height" type="number" label="Height (cm)"></v-text-field>
            <v-text-field v-model="weight" type="number" label="Weight (kg)"></v-text-field>
            <v-select v-model="activityLevel" :items="activityLevels" label="Activity Level"></v-select>
            <v-btn color="green darken-1" @click="calculateFitness">Calculate Fitness</v-btn>
          </v-form>
          <v-divider></v-divider>
          <v-alert v-if="bmr && tdee" :value="true" dense outlined>
            <p>Your Basal Metabolic Rate (BMR) is {{ bmr.toFixed(1) }} calories/day</p>
            <p>Your Total Daily Energy Expenditure (TDEE) is {{ tdee.toFixed(1) }} calories/day</p>
          </v-alert>
        </v-card-text>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      age: null,
      gender: null,
      height: null,
      weight: null,
      activityLevel: null,
      bmr: null,
      tdee: null,
      genders: ['Male', 'Female'],
      activityLevels: [
        { text: 'Sedentary (little or no exercise)', value: 1.2 },
        { text: 'Lightly Active (light exercise or sports 1-3 days/week)', value: 1.375 },
        { text: 'Moderately Active (moderate exercise or sports 3-5 days/week)', value: 1.55 },
        { text: 'Very Active (hard exercise or sports 6-7 days/week)', value: 1.725 },
        { text: 'Super Active (very hard exercise or sports, physical job or training twice a day)', value: 1.9 }
      ],
    };
  },
  methods: {
    calculateFitness() {
      if (this.gender === 'Male') {
        this.bmr = 88.362 + (13.397 * this.weight) + (4.799 * this.height) - (5.677 * this.age);
      } else if (this.gender === 'Female') {
        this.bmr = 447.593 + (9.247 * this.weight) + (3.098 * this.height) - (4.330 * this.age);
      }
      this.tdee = this.bmr * this.activityLevel;
    },
  },
};
</script>

<style scoped>
.fitness-calculator {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
