<script setup>
import AboutImage from '../components/AboutImage.vue'
</script>
<template>
 <AboutImage/>
 <h1 class="title">Please enter your e-mail below and we will be in touch!</h1>
  <div class="input">
    <input v-model="inputValue" type="text">
    <button v-on:click="handleButtonClick">Enter</button>
    <div id="message" v-if="showImage">
      Thank you!
      We will contact you at: {{ inputValue }}
    </div>
    <div class="img-container">
    <img :class="{'hidden': !showImage}" src="../assets/media/thumbsup.png" alt="Thumbs up from Mario">
  </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      inputValue: '',
      showImage: false
    }
  },
  methods: {
    handleButtonClick() {
      if (this.inputValue !== ''){
        this.showImage = true;
      }
    }
  }
}
</script>


<style scoped>
.hidden {
  display: none;
}
.title{
  display: flex;
  justify-content: center;
  margin-top: 5vh;
  color: #da2543;
  text-shadow: 2px 2px 18px #bd0e0ea1;
}
.input {
  margin-left: 40%;
  margin-top: 10vh;
  margin-bottom: 10vh;
}
#app > div.input > button {
  background-color: #da2543;
  color: #17cccc;
  border-color: #bd0e0ea1;
}
.img-container {
  display: flex;
  justify-content: center;
  margin-top: 20px;
}
#message {
  color: #da2543;
  margin-top: 20px;
}

</style>
