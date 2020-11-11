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
.top-enter-active {
  transition: all 1.5s;
}
.top-enter, .top-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  transform: translateY(40px);
}
.top-enter-to, .top-leave /* .fade-leave-active below version 2.1.8 */ {
  opacity: 1;
  transform: translateY(0px);
}


.top2-enter-active {
  transition: all 1s;
}
.top2-enter, .top2-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  transform: translateY(20px);
}
.top2-enter-to, .top2-leave /* .fade-leave-active below version 2.1.8 */ {
  opacity: 1;
  transform: translateY(0px);
}



.fade-enter-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
.fade-enter-to, .fade-leave /* .fade-leave-active below version 2.1.8 */ {
  opacity: 1;
}
</style>
