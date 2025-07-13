<script>
export default {
  data() {
    return {
      city: "",
      error: "",
    };
  },
  computed: {
    cityName() {
      return "<< " + this.city + " >>";
    },
  },
  methods: {
    getWeather() {
      if (this.city.trim().length < 2) {
        this.error = "Нужно название больше одного символа.";
        return false;
      }
      this.error = "";
    },
  },
};
</script>

<template>
  <div class="wrapper">
    <h1 class="title">Weather Application</h1>
    <p class="subtitle">
      Learn about weather in {{ city == "" ? "your city." : cityName }}
    </p>
    <div class="row">
      <input
        class="input"
        v-model="city"
        type="text"
        placeholder="Enter city"
        id="inputCity"
      />
      <button class="button" @click="getWeather()">Get weather</button>
    </div>
    <p class="error">{{ error }}</p>
  </div>
</template>

<style scoped>
.error {
  color: #d03939;
}
.wrapper {
  width: 900px;
  height: 500px;
  border-radius: 50px;
  background: #1f0f24;
  padding: 20px;
  text-align: center;
  color: #fff;
}

.title {
  margin-top: 50px;
}
.subtitle {
  margin-top: 20px;
}

.input {
  border: 0;
  border-bottom: 2px solid #110813;
  color: #fcfcfc;
  outline: none;
  padding: 5px 8px;
  background: transparent;
  padding: 10px;
  margin-top: 30px;
  font-size: 14px;
}

.input:focus {
  border-bottom-color: #6e2d7d;
}

.button {
  background: #e3bc4b;
  color: #fff;
  border-radius: 10px;
  border: 2px solid #b99935;
  padding: 10px 15px;
  margin-left: 20px;
  cursor: pointer;
  transition: transform 500ms ease;
}

.button:hover {
  transform: scale(1.1) translateY(-5px);
}
</style>
