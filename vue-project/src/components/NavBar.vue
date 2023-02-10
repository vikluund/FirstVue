<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <div id="navbar">
  <span class="toggle button">&#9776;</span>
    <ul>
      <li>
        <RouterLink to="/">Hem</RouterLink>
      </li>
      <li>
        <RouterLink to="/about">About</RouterLink>
      </li>
    </ul>
  </div>
  <RouterView />

</template>

<style scoped>
#navbar {
  margin: 0 auto;
  padding: 0;
  height: 10vh;
}
#navbar ul {
  display: flex;
  justify-content: center;
}
#navbar ul li {
  list-style: none;
  display: inline-block;
  padding: 0 100px;
}

#navbar ul li a {
  text-decoration: none;
  color: rgb(39, 169, 192);
  font-size: 2.5em;
}
#navbar ul li a:hover {
  color: rgb(21, 199, 101);
  font-weight: normal;
}
#navbar .toggle-button {
  display: none;
  position: absolute;
  right: 20px;
  top: 10px;
  cursor: pointer;
}
@media only screen and (max-width: 800px) {
  /* Show toggle button for smaller screens */
  #navbar .toggle-button {
    display: block;
  }

  /* Show navigation items */
  #navbar ul li {
    display: block;
    text-align: center;
    margin: 10px 0;
  }
}
</style>
