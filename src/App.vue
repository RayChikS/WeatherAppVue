<template>
  <div class="wrapper">
    <h1 class="title">Weather Application</h1>
    <p class="subtitle">Learn about weather in your city</p>
    <div class="row">
      <input
        class="input"
        type="text"
        placeholder="Enter city"
        id="inputCity"
      />
      <button type="button" class="inputBtn">Add</button>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
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
}
</style>
