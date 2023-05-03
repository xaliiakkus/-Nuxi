<template>
  <div class="bg-white">
    <div class=" box container flex items-center justify-center p-7 ">
      <div class="sl   ">
        <h2 class="font-bold py-2 lg:text-4xl text-3xl lg:leading-9 text-gray-800 ">What we did
        </h2>
        <p class="font-normal text-base leading-6 text-gray-600 mt-6 w-full lg:w-10/12 xl:w-9/12 text-left">
          TravelShop Booking invested to its own, completely new software and worked with the bests of the
          sector
          to simplify the booking process for both operators and travelling lovers.
          Today in the TravelShop Booking’s pages it is possible to find the best packegess, responsible
          operators, money safe tours and latest, interesting travelling contents througout the blog. However
          these are just the introduction of the story, the team is working to improve all services to boost
          the
          best travelling experince.
        </p>
      </div>
      <div class="sl ">
        <h2 class="font-bold py-2 lg:text-4xl text-3xl lg:leading-9  text-gray-800  ">What
          we aim for
        </h2>
        <p class="font-normal text-base leading-6 text-gray-600 w-full lg:w-10/12 xl:w-9/12  text-left">
          Travelling is not a holiday or a memorible, relaxing moments for us. It is some how to explore the
          univers we live in, to set up and raise ties with the people we never know and to enrich with the
          new
          cultures, beliefs and way of breaths. The aim that we are working to achieve is to make this
          possible
          via bringing people together with the tours to all around the world. So procuring new destinations,
          and
          flexible tours for every interest as well as make arrange them luxury or reasonable is the goal.
        </p>
      </div>
    </div>
    <div
      class="flex flex-col lg:flex-row items-stretch justify-between lg:px-0 px-6 lg:py-20 py-8 2xl:mx-auto 2xl:container">
      <div class="z-30 relative lg:w-1/2">
        <div
          class="  rounded-xl dark:bg-gray-800 bg-gray-100 w-full lg:w-10/12 lg:h-full lg:flex justify-end items-center">
          <div class=" w-full lg:w-auto lg:-mr-32 rounded-xl">
            <img src="/flags/news/AllNews.png" alt="image with decent chairs"
              class="w-full relative z-30 lg:pl-20 px-6 py-14 " />
          </div>
        </div>
        <div class="absolute top-0 dark:bg-gray-800 bg-gray-100 md:h-96 w-full hidden md:block lg:hidden">
        </div>
      </div>
      <div class="bg-gray-100 dark:bg-gray-800 lg:w-1/2 lg:ml-12 lg:p-14 p-8 flex items-center">
        <div>
          <h1
            class="dark:text-white md:w-8/12 lg:w-10/12 xl:8/12 2xl:w-8/12 w-full xl:text-6xl sm:text-5xl text-4xl font-semibold text-gray-800 capitalize">
            News</h1>
          <p
            class="dark:text-gray-300 md:w-9/12 lg:w-11/12 xl:w-10/12 2xl:9/12 text-base leading-normal text-gray-600 mt-5">
          </p>
          <router-link to="gallery">
            <button
              class="dark:bg-white dark:hover:bg-gray-400 dark:hover:text-gray-100 dark:text-gray-800 sm:w-auto w-full mt-8 text-base justify-between focus:ring-2 focus:ring-offset-2 focus:ring-gray-700 focus:outline-none hover:bg-gray-700 font-medium leading-none text-white py-4 px-8 bg-gray-800 flex items-center">
              <router-link to="news"> Explore</router-link>
            </button>
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
  data() {
    return {};
  },
};
</script>

<style lang="CSS" scoped>
@media screen and (min-width: 1200px) {
    .sl {
        width: 800px;
        height: 303px;
    }
}

/* Laptop */
@media screen and (min-width: 992px) and (max-width: 1199px) {
    .sl {
        width: 600px;
        height: 250px;

    }

}

/* Tablet */
@media screen and (min-width: 768px) and (max-width: 991px) {
    .sl {
        width: 450px;
        height: 225px;
        flex-direction: column;

    }
}

/* Mobil */
@media screen and (max-width: 390px) and (min-height:375px) {
    .sl {
        width: 350px;
        height: 185px;
        margin: 0 0 172px;
    }
    .box{

        justify-content: space-between;
        align-items: flex-start;
        flex-wrap: wrap;
    }
}


h1 {
    text-align: center;
    color: chocolate;
}

.flex-container {
    display: flex;
    flex-wrap: nowrap;

}


.flex-container>div {
    width: 800px;
    margin: 10px;
    height: 200px;
    text-align: center;
    line-height: 75px;
    font-size: 30px;
}
</style>
