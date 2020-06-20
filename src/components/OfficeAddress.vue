<template>
   <div>
      <h3>{{office.name}}</h3>
      <div class="address">
         {{office.address}}<br>
         {{office.postcode}}<br>
         {{office.country}}
      </div>
   </div>
</template>

<script>
export default {
  props: ["office"]
};
</script>
<style lang="scss" scoped>
@import url(//db.onlinewebfonts.com/c/3dd6e9888191722420f62dd54664bc94?family=Myriad+Pro);

h3 {
  font-size: 26px;
  font-weight: 300;
  color: #fff;
  text-align: left;
  margin-top: 55px;
  margin-bottom: 35px;
  text-transform: capitalize;
}

.address {
  min-width: 120px;
  font-size: 11px;
  color: #fff;
  font-family: "MyriadPro";
  text-align: left;
}
</style>