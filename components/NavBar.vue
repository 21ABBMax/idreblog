<template>
  <nav class="w-full fixed p-6 background-color shadow-2xl z-40">
    <div class="flex items-center justify-end md:justify-center">
      <!-- Mobile toggle -->
      <div class="md:hidden">
        <button @click="drawer">
          <svg
            class="h-8 w-8 fill-current text-black"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            viewBox="0 0 24 24"
            stroke="white"
          >
            <path d="M4 6h16M4 12h16M4 18h16"></path>
          </svg>
        </button>
      </div>

      <!-- Navbar -->
      <div
        class="hidden md:block text-white flex items-center jusify-center transform transition ease-in-out duration-500 hover:scale-110"
      >
        <ul class="flex space-x-8 text-sm font-sans">
          <li>
            <nuxt-link
              to="/"
              class="transform transition ease-in-out duration-700 hover:scale-105"
              >Home</nuxt-link
            >
          </li>
          <li>
            <nuxt-link to="/about_me" class="">About me</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/contact" class="">Contact me</nuxt-link>
          </li>
          <!-- <li><img class="" width="80px" height="80px" src="/images/vecteezy_mountain_1206236.png"></li> -->
        </ul>
      </div>

      <!-- Dark Background Transition -->
      <transition
        enter-class="opacity-0"
        enter-active-class="ease-out transition-medium"
        enter-to-class="opacity-100"
        leave-class="opacity-100"
        leave-active-class="ease-out transition-medium"
        leave-to-class="opacity-0"
      >
        <div
          @keydown.esc="isOpen = false"
          v-show="isOpen"
          class="z-10 fixed inset-0 transition-opacity"
        >
          <div
            @click="isOpen = false"
            class="absolute inset-0 bg-black opacity-60"
            tabindex="0"
          ></div>
        </div>
      </transition>

      <!-- Drawer Menu -->
      <aside
        class="p-5 transform text-white top-0 left-0 w-64 background-color-square fixed h-full overflow-auto ease-in-out transition-all duration-300 z-30"
        :class="isOpen ? 'translate-x-0' : '-translate-x-full'"
      >
        <div class="close">
          <button
            class="absolute top-0 right-0 mt-4 mr-4"
            @click="isOpen = false"
          >
            <svg
              class="w-6 h-6"
              fill="none"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              stroke="white"
            >
              <path d="M6 18L18 6M6 6l12 12"></path>
            </svg>
          </button>
        </div>

        <span
          @click="isOpen = false"
          class="flex w-full items-center p-4 border-b"
        >
          <Tailwind />
        </span>

        <ul class="divide-y font-sans">
          <li>
            <nuxt-link to="/" @click="isOpen = false" class="my-4 inline-block"
              >Home</nuxt-link
            >
          </li>
          <li>
            <nuxt-link
              to="/about_me"
              @click="isOpen = false"
              class="my-4 inline-block"
              >About me</nuxt-link
            >
          </li>
          <li>
            <nuxt-link
              to="/contact"
              @click="isOpen = false"
              class="my-4 inline-block"
              >Contact me</nuxt-link
            >
          </li>
          <li>
            <a
              href="https://www.abbgymnasiet.se/"
              target="blank_"
              class="my-8 w-full text-center font-semibold cta inline-block bg-yellow-100 hover:bg-yellow-200 px-3 py-2 rounded text-black"
              >My school</a
            >
          </li>
          <li>
            <nuxt-link
              to="/donate"
              @click="isOpen = false"
              class="my-8 w-full text-center font-semibold cta inline-block bg-gray-800 hover:bg-gray-700 px-3 py-2 rounded text-white"
              >Donate</nuxt-link
            >
          </li>
        </ul>

        <div class="follow">
          <p class="italic font-sans text-sm">follow me:</p>
          <div class="social flex space-x-5 mt-4">
            <a href="https://www.instagram.com/max.wigstein/" target="_blank">
              <svg
                aria-hidden="true"
                focusable="false"
                data-prefix="fab"
                data-icon="instagram"
                class="h-5 w-5 fill-current text-yellow-200"
                role="img"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
              >
                <path
                  fill="currentColor"
                  d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z"
                ></path>
              </svg>
            </a>
          </div>
        </div>
      </aside>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    drawer() {
      this.isOpen = !this.isOpen;
    },
  },
  watch: {
    isOpen: {
      immediate: true,
      handler(isOpen) {
        if (process.client) {
          if (isOpen) document.body.style.setProperty("overflow", "hidden");
          else document.body.style.removeProperty("overflow");
        }
      },
    },
  },
  mounted() {
    document.addEventListener("keydown", (e) => {
      if (e.keyCode == 27 && this.isOpen) this.isOpen = false;
    });
  },
};
</script>

<style>
.nuxt-link-exact-active {
  border-bottom: 3px solid rgb(253, 230, 138);
  border-radius: 1px;
  padding-bottom: 8px;
}

.background-color-square {
  background-color: rgb(34, 34, 34);
}

.background-color {
  background-color: rgb(42, 42, 42);
}
</style>
