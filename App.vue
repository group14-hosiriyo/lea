<template>
  
  <center>
   <div id="app" class="container">
    <div class="holder">

      <h1 style="color: gold;user-select: none;">BMI Calculator</h1>
      <div>
        <label for="weight">Weight (kg):</label><br><br>
        <input type="number" id="weight" v-model="weight"><br><br>
      </div>
      <div>
        <label for="height">Height (m):</label><br><br><br>
        <input type="number" id="height" v-model="height"><br><br>
      </div>
      <p>Your BMI is: {{ bmi }}</p><br>
      <p style="font-weight: 300px;">THANK YOU</p>
    </div>
  </div>
</center>
  </template>
  <script>
  
export default {
  data() {
    return {
      weight: null,
      height: null,
    };
  },
  computed: {
    bmi() {
      if (this.weight && this.height) {
        return (this.weight / (this.height ** 2));
      }
      return null;
    },
  }
};
</script>


