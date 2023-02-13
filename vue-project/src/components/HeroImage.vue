<script></script>
<template>
  <div id="hero-img">
    <img src="../assets/media/7225605.jpg" class="img-fluid" alt="Hero Image"/>
    <div class="hero-text">
      <h1>Welcome to the Project</h1>
    </div>
  </div>
</template>

<style scoped>
#hero-img img {
  margin: 0 auto;
  height: auto;
  overflow-x: hidden;
}
.hero-text{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #da2543;
}
.hero-text h1{
  font-size: 3.5em;
  font-weight: bold;
  text-shadow: 2px 2px 3px #000000a1;
}
</style>
