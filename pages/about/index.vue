<script>
import AboutHero from './AboutHero.vue'
import About from './About.vue'
import AboutPatner from './AboutPatner'
import Trustpilot from './Trustpilot.vue'
import Aboutwrite from './Aboutwrite.vue'

export default {
  name: 'About',
  components: {
    "Hero": AboutHero,
    "HomeCom": About,
    "Patner": AboutPatner,
    Aboutwrite,
    Trustpilot
  },
}
</script>
<template>
  <div>
    <div id="banner">
      <div id="banner-images"></div>
      <h1>About US</h1>
    </div>
    <section class="bg-white">
      <HomeCom />
      <Hero />
      <Aboutwrite />
      <Trustpilot />
      <Patner />
    </section>
  </div>
</template>

<style scoped>
@media screen and (min-width: 1200px) {
  #banner {
    width: 100%;
    height: 90px;
  }
}

/* Laptop */
@media screen and (min-width: 992px) and (max-width: 1199px) {
  #banner {
    width: 50%;
    height: 80px;
  }
}

/* Tablet */
@media screen and (min-width: 768px) and (max-width: 991px) {
  #banner {
    width: 35%;
    height: 50px;
  }
}

/* Mobil */
@media screen and (max-width: 380px) and (min-height:375px) {
  #banner {
    width: 25%;
    height: 50px;
  }
}

#banner {
  background-image: url(../../assets/images/about.jpg);
  height: 55vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

#banner #banner-images {
  height: 100%;
  position: relative;
  z-index: -10;
  filter: brightness(0.7) grayscale(0.6);
  animation: banner-change 15s infinite ease-in-out;
  display: flex;
  flex-direction: row;
}

#banner #banner-images img {
  width: 100vw;
  object-fit: cover;
}


#banner h1 {
  position: absolute;
  font-family: sans-serif;
  font-size: 40px;
  letter-spacing: 8px;
  color: rgb(230, 255, 255);
  text-shadow: 2px 2px 8px rgb(206, 206, 206);
  animation: color-cycle 5s infinite ease-in-out;
  color: rgb(233, 233, 233);
  text-transform: uppercase;
  margin-top: -14px;
  text-align: center;
  width: 90%;
}
</style>
