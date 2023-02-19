<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <nav class="navbar bg-body-tertiary fixed-top">
    <div class="container-fluid">
      <RouterLink class="navbar-brand" to="/">The First Vue</RouterLink>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="offcanvas"
        data-bs-target="#offcanvasNavbar"
        aria-controls="offcanvasNavbar"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div
        class="offcanvas offcanvas-end"
        tabindex="-1"
        id="offcanvasNavbar"
        aria-labelledby="offcanvasNavbarLabel"
      >
        <div class="offcanvas-header">
          <h5 class="offcanvas-title" id="offcanvasNavbarLabel">
            The First Vue
          </h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="offcanvas"
            aria-label="Close"
          ></button>
        </div>
        <div class="offcanvas-body">
          <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
            <li class="nav-item">
              <RouterLink class="nav-link active" aria-current="page" to="/"
                >Home</RouterLink
              >
            </li>
            <li class="nav-item">
              <RouterLink class="nav-link" to="/about">About</RouterLink>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>
  <RouterView />
</template>

<style scoped>
.navbar-brand {
  color: #da2543;
  text-shadow: 2px 2px 5px #bd0e0ea1;
  font-size: 1.5em;
}
.offcanvas-title {
  color: black;
}
.navbar-toggler {
  color: #17cccc;
  background-color: #da2543;
  box-shadow: 2px 2px 3px #000000a1;
}
button.navbar-toggler {
  color: #17cccc;
}
span.navbar-toggler-icon {
  color: #17cccc;
}
#offcanvasNavbar > div.offcanvas-header {
  background-color: rgb(20, 20, 20);
}
#offcanvasNavbar > div.offcanvas-body {
  background-color: rgb(27, 27, 27);
}
#offcanvasNavbarLabel {
  color: #da2543;
  text-shadow: 2px 2px 5px #bd0e0ea1;
}
#offcanvasNavbar > div.offcanvas-body > ul > li:nth-child(1) > a {
  color: #da2543;
  text-shadow: 2px 2px 5px #bd0e0ea1;
}
#offcanvasNavbar > div.offcanvas-body > ul > li:nth-child(1) > a:hover {
  color: #17cccc;
}
#offcanvasNavbar > div.offcanvas-body > ul > li:nth-child(2) > a {
  color: #da2543;
  text-shadow: 2px 2px 5px #bd0e0ea1;
}
#offcanvasNavbar > div.offcanvas-body > ul > li:nth-child(2) > a:hover {
  color: #17cccc;
}
#offcanvasNavbar > div.offcanvas-header > button {
  background-color: #da2543;
  text-shadow: 2px 2px 5px #bd0e0ea1;
}
</style>
