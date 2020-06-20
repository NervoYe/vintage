<template>
   <div class="contacts-container">
      <h1>Contacts</h1>
      <div class="contacts__columns">
         <div class="contacts__row">
            <h2><span class="green">GMS</span> Headquarters</h2>
            <div class="contacts__row--column">
               <div class="contacts__info first">
                  <div class="contacts__address">Global Message Services Ukraine LLC<br>
                     Bundesstrasse 5 | 3rd Floor<br>
                     6300 Zug<br>
                     Switzerland</div>
                  <div class="phone"> <a class="link"
                      href="tel:+41415446200">+41 41 544 62 00</a></div>
               </div>
               <div class="contacts__info">
                  <div>Email<br> <a class="link link--bold"
                      href="mailto:info@gms-worldwide.com">info@gms-worldwide.com</a>
                  </div>
                  <div>Send message<br><a class="link link--bold"
                      :href="viberLink">Viber us</a></div>
                  <div>Send form<br>
                     <a class="link link--bold"
                      href="#form">Contact us</a></div>
               </div>
            </div>
         </div>
         <div class="contacts__row">
            <h2>Technical support <span class="green">24/7</span></h2>
            <div class="contacts__tech">GMS understands that it can be hard to follow all new technologies. We regularly provide for all our clients educational trainings to make your operator`s business earn more and better though our best practices.</div>
            <div class="phone"><a class="link"
                href="tel:+41415446206">+41 41 544 62 06</a></div>
         </div>
      </div>
   </div>
</template>

<script>
export default {
  computed: {
    viberLink() {
      if (
        /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(
          window.navigator.userAgent
        )
      ) {
        return "viber://add?number=41415446200";
      } else {
        return "viber://chat?number=%2B41415446200";
      }
    }
  }
};
</script>

<style lang="scss" scoped>
$font-color: #333333;
$green-color: #3db565;

.contacts-container {
  background-color: #fff;
  max-width: 1280px;
  padding: 60px;
  padding-bottom: 100px;
  color: $font-color;
}

h1 {
  font-size: 50px;
  font-weight: 300;
}

.contacts__columns {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  align-items: stretch;

  .contacts__row {
    flex-basis: 48%;

    h2 {
      font-size: 34px;
      font-weight: 300;
      margin-top: 50px;
      margin-bottom: 45px;
    }
  }
}

.contacts__row--column {
  @extend .contacts__columns;
  align-content: space-between;
  min-height: 200px;

  .contacts__info {
    min-height: 155px;
    font-size: 15px;
    font-weight: 300;
    line-height: 1.87;
  }
}

.first {
  display: flex;
  flex-flow: column nowrap;
  align-content: space-between;
  justify-content: flex-end;
}
.green {
  color: $green-color;
}

.link {
  color: $green-color;
  text-decoration: none;
  text-transform: uppercase;

  &:hover {
    color: #00ff7f;
  }

  &:visited {
    color: #2e8b57;
  }
}

.link--bold {
  font-weight: 600;
}

.phone {
  @extend .link;
  font-size: 26px;
  padding-top: 15px;
  font-weight: 300;
}

.contacts__tech {
  text-align: justify;
  margin-bottom: 35px;
}

@media (max-width: 550px) {
  h1 {
    text-align: center;
  }
  .contacts__columns {
    flex-flow: column nowrap;
    align-items: center;
    justify-content: center;
    align-items: center;
  }

  .contacts__row--column {
    flex-flow: column nowrap;
    align-items: center;
    justify-content: center;
    align-items: center;
  }
  h2 {
    text-align: center;
  }
  .contacts__info {
    margin: 25px 0;
    text-align: center;
  }

  .phone {
    text-align: center;
  }
}
</style>