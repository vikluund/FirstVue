<script setup>
import HeroImage from "../components/HeroImage.vue";
import TheCharacters from "../components/TheCharacters.vue";
</script>

<template>
  <HeroImage />
  <h1 class="title">{{ message }}</h1>
  <div id="cards">
    <div class="container text-center">
      <div class="row align-items-start">
        <the-characters
          v-for="character in characters"
          :key="character.id"
          :char="character"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      message: "Some of the classic pixel games",
      characters: [],
    };
  },
  components: { "the-characters": TheCharacters },
  mounted() {
    this.fetchData();
  },
  methods: {
    async fetchData() {
      const response = await fetch("data.json");
      const result = await response.json();
      this.characters = result;
    },
  },
};
</script>
<style scoped>
#cards {
  display: flex;
  justify-content: center;
  margin-top: 10vh;
  margin-bottom: 10vh;
}
.title {
  display: flex;
  justify-content: center;
  margin-top: 15vh;
  color: #da2543;
  font-size: 4em;
  text-shadow: 2px 2px 5px #bd0e0ea1;
}
</style>
