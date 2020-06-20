<template>
   <div id="app">
      <Offices />
   </div>
</template>

<script>
import Offices from "./views/Offices.vue";

export default {
  name: "App",
  components: {
    Offices
  }
};
</script>

<style lang="scss">
@import url(//db.onlinewebfonts.com/c/88f10bf18a36407ef36bf30bc25a3618?family=Suisse+Intl);
@import url(//db.onlinewebfonts.com/c/653d9381828e9577fb1e417dc047f89d?family=Suisse+Intl+SemiBold);
$font-color: #333333;
$green-color: #3db565;

#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: "Suisse Intl";
}
</style>

