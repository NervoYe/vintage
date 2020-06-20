<template>
   <div class="offices-container">
      <div class="columns">
         <h2>our offices</h2>
         <div class="common">
            <div class="left">
               <ul class="nav-tabs">
                  <li @click="currentTab = 'kyiv'"><a href="#">Kyiv</a></li>
                  <li @click="currentTab = 'newYork'"><a href="#">New York</a></li>
                  <li @click="currentTab = 'guangzhou'"><a href="#">Guangzhou</a></li>
                  <li @click="currentTab = 'barcelona'"><a href="#">Barcelona</a></li>
               </ul>

               <div class="tab-content">
                  <div v-if="currentTab === 'kyiv'">
                     <OfficeAddress :office="offices[0]" />
                  </div>
                  <div v-if="currentTab === 'newYork'">
                     <OfficeAddress :office="offices[1]" />
                  </div>
                  <div v-if="currentTab === 'guangzhou'">
                     <OfficeAddress :office="offices[2]" />
                  </div>
                  <div v-if="currentTab === 'barcelona'">
                     <OfficeAddress :office="offices[3]" />
                  </div>
               </div>
            </div>
            <div class="right">123</div>
         </div>
      </div>
   </div>
</template>

<script>
import OfficeAddress from "../components/OfficeAddress.vue";

export default {
  components: {
    OfficeAddress
  },
  data: () => ({
    currentTab: "kyiv",
    offices: [
      {
        city: "kyiv",
        name: "Global Message Services Ukraine LLC",
        address: "Kyiv, Stepan Bandera, 33",
        postcode: "02066",
        country: "Ukraine",
        coordinate: ""
      },
      {
        city: "New York",
        name: "Global Message Services USA LLC",
        address: "New York, Wall Street, 33",
        postcode: "12587",
        country: "USA",
        coordinate: ""
      },
      {
        city: "Guangzhou",
        name: "Global Message Services China LLC",
        address: "Guangzhou, China Town, 1",
        postcode: "00054",
        country: "China",
        coordinate: ""
      },
      {
        city: "Barcelona",
        name: "Global Message Services Spain LLC",
        address: "Barcelona, Sunny Beach, 2",
        postcode: "02066",
        country: "Spain",
        coordinate: ""
      }
    ]
  })
};
</script>
<style lang="scss" scoped>
$green-color: #3db565;

.offices-container {
  background-color: #262626;
  width: 100vw;
  min-height: 500px;
  padding: 60px;
  padding-bottom: 100px;
  color: #fff;

  .columns {
    max-width: 1280px;
    margin: 0 auto;
    padding: 60px;
    padding-bottom: 100px;

    .common {
      display: flex;
      flex-flow: row nowrap;
      justify-content: space-between;
      align-items: stretch;

      .left,
      .right {
        flex-basis: 48%;
      }
    }
  }
}

h2 {
  text-transform: capitalize;
  font-size: 34px;
  font-weight: 300;
  text-align: left;
}

.nav-tabs {
  padding: 0;
}

li {
  display: inline-block;
  padding: 0 15px;
  font-weight: bold;
  text-transform: uppercase;
}

li:first-child {
  padding-left: 0;
}

a {
  text-decoration: none;
  color: #fff;
  &:hover {
    color: aqua;
  }

  &:visited {
    color: blue;
  }
}
</style>