<template>
  <div id="app">
    <Header></Header>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import Header from "@/components/Header/Header.vue";

export default {
  name: "Home",
  components: {
    Header,
  },
};
</script>

<style lang="scss">
@import "@/styles/normalize.scss";
@import "@/styles/vars.scss";
@font-face {
  font-family: Daniel;
  src: url(./fonts/daniel.regular.otf);
}
@font-face {
  font-family: Trebuchet MS;
  src: url(./fonts/trebuschet.ttf);
}
@font-face {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  src: url(./fonts/verdana.TTF);
}
@font-face {
  font-family: Ardleys Hand;
  src: url(./fonts/ArdleysHand.ttf);
}
@font-face {
  font-family: Pacifico-Regular;
  src: url(./fonts/Pacifico-Regular.ttf);
}
@font-face {
  font-family: Tahoma;
  src: url(./fonts/TAHOMA.TTF);
}
.main-page-inner {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 10px;
  height: 100%;
}
body {
  background-color: #e2e1da;
  font-family: "Trebuchet MS";
  color: $grey-text;
}
</style>
