<template>
  <v-app>
    <AppHeader />
    <AppMain />
  </v-app>
</template>

<script>
import AppMain from "./components/AppMain";
import AppHeader from "./components/AppHeader";

export default {
  components: { AppMain, AppHeader },
}
</script>

<style>
html {
  scroll-behavior: smooth;
}
@font-face {
  font-family: 'b nazanin';
  src: url('http://cdn.bayan.ir/blog/templates/shared/fonts/BNazanin.eot?view#iefix') format('embedded-opentype'),
  url('http://cdn.bayan.ir/blog/templates/shared/fonts/BNazanin.woff?view') format('woff'),
  url('http://cdn.bayan.ir/blog/templates/shared/fonts/BNazanin.ttf?view') format('truetype');
}

#app {
  font-family: 'b nazanin';
}
</style>
