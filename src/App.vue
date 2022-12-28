<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue';

</script>

<template>
  <div class="content">
  <header>

    <div class="header">
        <a class="logo">Dylan Stevens</a>
        <div class="header-right">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/contact">Contact</RouterLink>
        <RouterLink to="/projects">Projects</RouterLink>
        </div>
    </div>
  </header>
  <div class="bd">
    <RouterView />
  </div>
  </div>
</template>

<style>


  .header {
  overflow: hidden;
  background: rgb(19,35,66);
  background: linear-gradient(90deg, rgba(19,35,66,1) 0%, rgb(23, 30, 45) 47%, rgba(45,45,49,1) 100%);
  padding: 40px 20px;
  min-height: 50px;
  }

  /* Style the header links */
  .header a {
  float: left;
  color: white;
  text-align: center;
  padding: 12px;
  text-decoration: none;
  font-size: 18px;
  line-height: 25px;
  border-radius: 4px;
  transition: 0.3s;
  position: relative;
  }

  .header a::before {
      content: "";
      position: absolute;
      display: block;
      width: 100%;
      height: 2px;
      bottom: 0;
      left: 0;
      background-color: rgba(245, 245, 245, 1);
      transform: scaleX(0);
      transition: transform 0.5s ease;
  }

  /* Style the logo link (notice that we set the same value of line-height and font-size to prevent the header to increase when the font gets bigger */
  .header a.logo {
  font-size: 28px;
  font-weight: 300;
  font-family: 'Raleway', sans-serif;
  transition: 0.3s;
  }

  /* Change the background color on mouse-over */
  .header a:hover::before {
  transform: scale(1);
  }

  /* Style the active/current link*/
  .header a.router-link-active {
  box-shadow: 0 0 20px 0 rgba(25, 25, 25, 1);
  border-radius: 12px;
  color: white;
  font-family: 'Raleway', sans-serif;
  }

  /* Float the link section to the right */
  .header-right {
  float: right;
  font-family: 'Raleway', sans-serif;
  
  }

  /* Add media queries for responsiveness - when the screen is 500px wide or less, stack the links on top of each other */
  @media screen and (max-width: 540px) {
  .header {
      min-height: 200px;
  }
  .header a {
      float: none;
      display: block;
      text-align: left;
  }
  .header-right {
      float: none;
  }
  }
</style>
