<template>
  <div>
    <div class="bg-white border-gray-200 dark:bg-gray-900">

      <div class="2xl:flex xl:flex space-x-10 gap-32 justify-center lg:flex md:grid xs:grid xxs:grid ">
        <div :class="{ '': !isNavbarOpen, 'w-full': true }">
          <ul
            class="2xl:flex xl:flex  justify-center lg:flex md:grid xs:grid xxs:grid xl:gap-64 2xl:gap-64 lg:gap-32 xxs:gap-2 xs:gap-3 sm:gap-5 ">
            <li class="m-2 px-5">
              <div id="P">
                <router-link
                  class="block py-2 pl-3 pr-4 xl:text-xl xs:text-sm  cursor-pointer   text-gray-900 rounded md:border-0"
                  to="news">Press Relase</router-link>
              </div>
            </li>
            <li class="m-2 px-5">
              <div id="P">
                <router-link
                  class="block py-2 pl-3 pr-4 xl:text-xl xs:text-sm  cursor-pointer   text-gray-900 rounded md:border-0 "
                  to="event">Rewards</router-link>
              </div>
            </li>
            <li class="m-2 px-5">
              <div id="P">
                <router-link
                  class="block py-2 pl-3 pr-4 xl:text-xl xs:text-sm  cursor-pointer text-gray-900 rounded md:border-0"
                  to="workshops">WorkShops</router-link>
              </div>
            </li>
            <li class="m-2 px-5">
              <div id="P">
                <router-link
                  class="block py-2 pl-3 pr-4 xl:text-xl xs:text-sm  cursor-pointer   text-gray-900 roundedmd:border-0"
                  to="Contact">Contact</router-link>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <hr class="w-full h-1 bg-cyan-500">
    <div class="bg-white 2xl:mx-auto lg:py-16 lg:px-20 md:py-12 md:px-6 py-9 px-4">
      <div class="flex lg:flex-row flex-col lg:gap-8 sm:gap-10 gap-12">
        <div class="w-full xl:m-20 lg:w-6/12">
          <h2 class="w-full font-bold lg:text-4xl text-3xl lg:leading-10 leading-9 text-left">A brief story of us…
          </h2>
          <p class="font-normal text-base leading-6 text-gray-600 mt-6 text-left">
            The inception of TSG dates back to its origins in the Bodrum district, a popular tourist destination
            in Turkey that attracts both domestic and international visitors. Prior to its establishment as a
            tourism company, we worked as a group leader from 1990 to 2005, arranging daily recreational
            activities. Our ardor for travel blossomed in 2005 when we began hosting numerous guests at the
            Bodrum Kalender Hotel for seven years. This experience taught us the intricacies of tourism and we
            became self-made professionals.
          </p>
        </div>
        <div class="w-full lg:w-6/12">
          <video controls autoplay style="border-radius: 25px; width:100%;">
            <source src="/flags/4x3/video.mp4" type="video/mp4">
            Download the
            or
            <a href="/flags/4x3/video.mp4">MP4</a>
            video.
          </video>
        </div>
      </div>
      <Contents />

    </div>
  </div>
</template>

<script >
import Contents from './Contents.vue'

export default {
  name: 'Write',
  data() {
    return {
      isNavbarOpen: false, // Başlangıçta navbar kapalı durumda
      SortText: ``,
      SortTextActived: false,
    };
  },
  methods: {
    ActivedSortText() {
      this.SortTextActived = true;
    }
    ,
    toggleNavbar() {
      this.isNavbarOpen = !this.isNavbarOpen; // Navbar durumunu tersine çevir
    },
  },
  components: {
    Contents
  }
}
</script>

<style lang="scss" scoped>
.space {
  display: flex;
  gap: 60px;
}

#P {

  color: #42b9d6;
  font-family: inherit;
  font-weight: 800;
  cursor: pointer;
  position: relative;
  border: none;
  background: none;
  transition-timing-function: cubic-bezier(0.25, 0.8, 0.25, 1);
  transition-duration: 400ms;
  transition-property: color;
}

#P:focus,
#P:hover {
  color: #fff;
}

#P:focus:after,
#P:hover:after {
  width: 100%;
  left: 0%;
}

#P:after {
  content: "";
  pointer-events: none;
  bottom: -2px;
  left: 50%;
  position: absolute;
  width: 0%;
  height: 2px;
  background-color: #96d7eb;
  transition-timing-function: cubic-bezier(0.25, 0.8, 0.25, 1);
  transition-duration: 400ms;
  transition-property: width, left;
}
</style>
