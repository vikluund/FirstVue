<script></script>
<template>
  <div id="hero-img">
    <img
      src="../assets/media/FarOldElephantbeetle-max-1mb.gif"
      class="img-fluid"
      alt="Hero Image"
    />
    <div class="hero-text">
      <h1>WELCOME</h1>
    </div>
  </div>
</template>

<style scoped>
#hero-img {
  position: relative;
}
#hero-img img {
  margin: 0 auto;
  height: auto;
  width: 100%;
  overflow-x: hidden;
}
#hero-img::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.3);
}
.hero-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #da2543;
}
.hero-text h1 {
  font-size: 6.5em;
  font-weight: bold;
  letter-spacing: 0.05em;
  text-shadow: 2px 2px 18px #bd0e0ea1;
}
</style>
