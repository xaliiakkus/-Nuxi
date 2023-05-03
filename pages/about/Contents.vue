<template>
  <div
    class="xs:px-20 sm:px-20 md:px-20 lg:px-20 xs:justify-center  xl:justify-between  flex xs:flex-wrap bg-transparent py-8">
    <div class="xxs xl:p-16  lg:p-16 md:p-16 sm:flex-wrap xs:flex-wrap" v-for="(slide, i) in slides" :key="i">
      <div class=" ">
        <a class=" xs:flex-row ">
          <div class="mt-2">
            <img :src="slide.image" id="tourCardImg" class="" />
            <dl>
              <div>
                <dt class="sr-only"></dt>
                <dd class="  text-xl items-center text-center text-[#000000]">
                  {{ slide.value }}
                </dd>
                <dd class="text-large text-gray-500"></dd>
              </div>
              <div>
                <dd class=" text-xl items-center text-center text-[#42b9d6]" max-length="8">
                  {{ slide.name }}
                </dd>
              </div>
            </dl>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Contents',
  data() {
    return {
      slides: [
        { name: 'Countries', value: '160 +', image: '/flags/4x3/jug1.png ' },
        { name: 'Adventures', value: '10,000 +', image: '/flags/4x3/jug2.png ' },
        { name: 'Operators', value: '680 +', image: '/flags/4x3/jug3.png ' },
        { name: 'Custormer Happy ', value: '100%', image: '/flags/4x3/jug4.png ' },
        { name: 'Team Members', value: '140 +', image: '/flags/4x3/jug5.png ' },
      ],
    }
  },

}
</script>

<style lang="scss" scoped>
/* Masaüstü */
@media screen and (min-width: 1200px) {
  img {

    height: 100px;
    /* Örnek olarak 150 piksel yükseklik */
  }
}

/* Laptop */
@media screen and (min-width: 992px) and (max-width: 1199px) {
  img {
    width: 100px;
    /* Örnek olarak 80 piksel genişlik */
    height: 80px;
    /* Örnek olarak 120 piksel yükseklik */
  }
}

/* Tablet */
@media screen and (min-width: 768px) and (max-width: 991px) {

  img {
    width: 100px;
    /* Örnek olarak 60 piksel genişlik */
    height: 60px;
    /* Örnek olarak 90 piksel yükseklik */
  }
}

/* Mobil */
@media screen and (max-width: 380px) and (min-height:375px) {
  .xxs {
    flex-direction: column;

  }
}

.ps-16 {
  padding-inline-start: 4rem;
  font: bold 150px;
  font-weight: bold;

}

.flex-container {
  display: flex;
  flex-wrap: nowrap;
  background-color: transparent;
}

.flex-container>div {
  background-color: transparent;
  width: 100px;
  margin: 10px;
  text-align: center;

}

.flex-container {
  display: flex;
  flex-wrap: nowrap;
  background: #feecd0;

}

hr {
  width: 70px;
  rotate: 90deg;
  margin: 80px;
}

.flex-container>div {
  background-color: #feecd0;
  width: 500px;
  margin: 10px;
  height: 200px;
  text-align: center;
  line-height: 75px;
  font-size: 30px;
}
</style>
