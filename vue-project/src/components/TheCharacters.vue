<template>
  <div class="col">
    <div class="card" style="width: 18rem;">
      <img :src="char.image" class="card-img-top" alt="..." />
      <div class="card-body">
        <h5 class="card-title">{{ char.name }}</h5>
        <h5 class="card-title">{{ char.year }}</h5>
        <p class="card-text">
          {{ char.info }}
        </p>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    props: {
      char: {
        required: true,
        type: Object
      }
    }
  }
</script>
<style scoped>
#cards > div > div > div > div {
  border-style: none;
  border-radius: 0%;
  background-color: #1a1919;
  text-shadow: 2px 2px 5px #bd0e0ea1;
}
#cards > div > div > div > div > div{
  border-radius: 2%;
  background-color: #1a1919;
}
#cards > div > div > div > div > div > h5{
  color: #17cccc;
}
#cards > div > div > div > div > div > p{
  color: #da2543;
}
#cards > div > div > div > div > img{
  background-color: #1a1919;
}
</style>
