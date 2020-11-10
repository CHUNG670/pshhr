<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  margin: 0;
  padding: 0;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
*{
  margin: 0;
  padding: 0;
}
.top-enter-active, .top-leave-active {
  transition: opacity .5s;
}
.top-enter, .top-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 1;
}
</style>
