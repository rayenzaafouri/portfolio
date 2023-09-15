<template>

  <router-view/>
</template>

<style>
body{
  margin: 0;
  color: black;
  min-height: 100dvh;
  }
  body:nth-child(2) {
    margin-top: 4em;
  }

  .navbar-safe{
    display: block;
    height: 1em;
  }

/* Responsive shit*/

@media screen and (min-width: 1024px) {
  .dev-intro{
        transform: scale(0.75);
}
}
</style>
