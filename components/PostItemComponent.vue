<template>
  <div
    style=""
    class="w-56 border-4 border-yellow-100 transform transition ease-in-out duration-700 hover:scale-105 rounded-md"
  >
    <div class="">
      <img
        class="rounded-sm"
        :src="item.image"
        alt="post image"
        style="color: white"
      />
    </div>
    <div class="background-color rounded-md">
      <div class="flex justify-center">
        <h2 class="text-lg" style="color: white; text-decoration: underline">
          {{ item.title }}
        </h2>
      </div>
      <div class="flex justify-center mr-4 ml-4">
        <p class="text-white">{{ item.description }}</p>
      </div>
    </div>

    <!-- <img src="../assets/pictures/DFS-BFS/grafo.jpg" alt=""> -->
  </div>
</template>

<script>
export default {
  props: ["item"],

  data() {
    return {};
  },
};
</script>

<style></style>
