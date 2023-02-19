<script></script>
<template>
  <div id="about-img">
    <img src="../assets/media/mario-pixel-art-digital-art-nintendo-computer-uhdpaper.com-4K-4.2038.jpg" class="img-fluid" alt="About us hero image"/>
    <div class="about-text">
      <h1>Contact us</h1>
    </div>
  </div>
</template>
<style scoped>
#about-img {
  position: relative;
}
#about-img img {
  margin: 0 auto;
  height: auto;
  width: 100%;
  overflow-x: hidden;
}
#about-img::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.3);
}
.about-text{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #da2543;
}
.about-text h1{
  font-size: 6.5em;
  font-weight: bold;
  letter-spacing: 0.05em;
  text-shadow: 2px 2px 18px #bd0e0ea1;
}
</style>
