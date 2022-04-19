<template>
  <div class="min-h-screen">
    <div
      class="bg-fixed h-screen w-full sm:w-full bg-cover bg-top"
      style="background-image: url(/images/Meny-Mountain-Fog.jpg)"
    >
      <div
        class="bg-black bg-opacity-40 w-full h-full flex justify-center items-center flex-col"
      >
        <div class="flex justify-center flex-col">
          <h1
            class="text-white md:text-6xl text-4xl flex justify-center font-light animate-bounce"
          >
            WELCOME TO IDRE
          </h1>
          <div class="flex justify-center text-white animate-pulse">
            <h2>WHERE THE ADVENTURE BEGINS</h2>
          </div>
        </div>

        <div class="flex flex-row gap-24 mt-8">
          <div class="flex flex-row items-center">
            <h1
              class="cta background-color px-3 py-2 text-white font-semibold shadow-lg"
            >
              Donate
            </h1>
            <nuxt-link
              to="/donate"
              class="cta background-color hover:bg-gray-700 px-3 py-2 text-white font-semibold shadow-lg"
              >></nuxt-link
            >
          </div>

          <div class="flex flex-row items-center">
            <h1
              class="cta bg-yellow-100 px-3 py-2 text-black font-semibold shadow-lg"
            >
              My school
            </h1>
            <a href="https://www.abbgymnasiet.se/" target="blank_"
              ><h1
                class="cta bg-yellow-100 hover:bg-yellow-200 px-3 py-2 text-black font-semibold shadow-lg"
              >
                >
              </h1></a
            >
          </div>
        </div>
        <svg
          class="h-1/12 w-1/12 mt-64 animate-bounce svgStyle absolute"
          version="1.1"
          id="Capa_1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          x="0px"
          y="0px"
          viewBox="0 0 490.4 490.4"
          style="enable-background: new 0 0 490.4 490.4"
          xml:space="preserve"
          fill="white"
        >
          <g>
            <g>
              <path
                d="M490.4,245.2C490.4,110,380.4,0,245.2,0S0,110,0,245.2s110,245.2,245.2,245.2S490.4,380.4,490.4,245.2z M24.5,245.2
			c0-121.7,99-220.7,220.7-220.7s220.7,99,220.7,220.7s-99,220.7-220.7,220.7S24.5,366.9,24.5,245.2z"
              />
              <path
                d="M253.9,360.4l68.9-68.9c4.8-4.8,4.8-12.5,0-17.3s-12.5-4.8-17.3,0l-48,48V138.7c0-6.8-5.5-12.3-12.3-12.3
			s-12.3,5.5-12.3,12.3v183.4l-48-48c-4.8-4.8-12.5-4.8-17.3,0s-4.8,12.5,0,17.3l68.9,68.9c2.4,2.4,5.5,3.6,8.7,3.6
			S251.5,362.8,253.9,360.4z"
              />
            </g>
          </g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
          <g></g>
        </svg>
      </div>
    </div>
    <div class="min-h-screen">
      <div id="Heading-blog" class="text-6xl text-center text-white">
        <h1 class="underline italic mt-20">Blogs</h1>
      </div>
      <div
        class="flex justify-center mt-8 text-white italic md:text-normal text-sm"
      >
        <h3 class="animate-pulse">
          *Note that these pictures may not represent the real deal
        </h3>
      </div>
      <div class="flex justify-center mt-32 md:text-xl">
        <h3 class="text-white italic animate-bounce">
          Please click on the category that you want to read
        </h3>
      </div>

      <div>
        <div
          class="mx-auto mt-20 md:w-3/4 lg:w-2/4 mt-20 shadow-2xl mt-20 transform transition ease-in-out duration-700 hover:scale-105"
        >
          <a href="/summer-blogs">
            <div class="flex flex-wrap">
              <div class="background-color-square w-full md:w-1/2 h-96 p-12">
                <div class="flex justify-center text-white flex-col">
                  <h2 class="text-xl">Summer Collection</h2>
                  <h3 class="mt-4 italic text-sm">
                    When you want to enjoin the Summer
                  </h3>
                  <hr class="mt-6 w-16" />
                  <p class="italic text-sm mt-4">
                    The summer in Idre is something else.<br />With the tall
                    mountains, green forrests and the thousands of lakes.
                  </p>
                </div>
              </div>
              <div class="w-full md:w-1/2 h-96 border-4 md:mt-0 md:border-0">
                <img
                  class="bg-cover h-full w-full shadow-inner"
                  src="/images/river-foggy-mountains-landscape.jpg"
                  alt=""
                />
              </div></div
          ></a>
          <a href="/summer-blogs">
            <div class="flex flex-wrap">
              <div
                class="w-full md:w-1/2 h-96 mt-4 border-4 md:mt-0 md:border-0"
              >
                <img
                  class="bg-cover h-full w-full shadow-inner"
                  src="https://cdn.pixabay.com/photo/2018/09/18/11/20/autumn-3685929_960_720.jpg"
                  alt=""
                />
              </div>
              <div class="background-color-square w-full md:w-1/2 h-96 p-10">
                <div class="flex justify-center text-white flex-col">
                  <h2 class="text-xl">Autumn Collection</h2>
                  <h3 class="mt-4 italic text-sm">
                    When you want to enjoin the Autumn
                  </h3>
                  <hr class="mt-6 w-16" />
                  <p class="italic text-sm mt-4">
                    The Autumn in Idre is very colorfull and cozy. With
                    colorfull trees, cold mornings, and the warm cup of coffe at
                    the campfire.
                  </p>
                </div>
              </div>
            </div></a
          >
        </div>
        <div
          class="mx-auto mt-20 md:w-3/4 lg:w-2/4 mt-20 shadow-2xl mt-20 transform transition ease-in-out duration-700 hover:scale-105"
        >
          <a href="/winter-blogs">
            <div class="flex flex-wrap">
              <div class="background-color-square w-full md:w-1/2 h-96 p-12">
                <div class="flex justify-center text-white flex-col">
                  <h2 class="text-xl">Winter Collection</h2>
                  <h3 class="mt-4 italic text-sm">
                    When you want to enjoin the Winter
                  </h3>
                  <hr class="mt-6 w-16" />
                  <p class="italic text-sm mt-4 mb-8">
                    The Winter time in Idre is beautiful. A meter of snow
                    whereever you look, and the fact that you can take the
                    snowmobile and enjoin the places that you never could
                    before.
                  </p>
                </div>
              </div>
              <div class="w-full md:w-1/2 h-96 border-4 md:mt-0 md:border-0">
                <img
                  class="bg-cover h-full w-full shadow-inner"
                  src="/images/NorthenLights.jpg"
                  alt=""
                />
              </div></div
          ></a>
          <a href="winter-blogs"
            ><div class="flex flex-wrap">
              <div
                class="w-full md:w-1/2 h-96 mt-4 border-4 md:mt-0 md:border-0"
              >
                <img
                  class="bg-cover h-full w-full shadow-inner"
                  src="https://cdn.pixabay.com/photo/2018/01/06/19/02/drop-3065629_960_720.jpg"
                  alt=""
                />
              </div>
              <div class="background-color-square w-full md:w-1/2 h-96 p-10">
                <div class="flex justify-center text-white flex-col">
                  <h2 class="text-xl">Spring Collection</h2>
                  <h3 class="mt-4 italic text-sm">
                    When you want to enjoin the Spring
                  </h3>
                  <hr class="mt-6 w-16" />
                  <p class="italic text-sm mt-4">
                    The Spring in Idre is the time of the year you can sit for
                    hours and hours staring at the melting snow, and the ground
                    showing up below.
                  </p>
                </div>
              </div>
            </div></a
          >
        </div>
      </div>
    </div>
    <FooterComp />
  </div>
</template>

<script>
import FooterComp from "~/components/FooterComp.vue";
export default {
  components: { FooterComp },
  name: "IndexPage",
};
</script>

<style>
.svgStyle {
  height: 10%;
  width: 10%;
}
hr {
  height: 2px;
  background-color: white;
}
</style>
