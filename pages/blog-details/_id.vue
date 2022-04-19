<template>
  <div>
    <div class="min-h-screen flex justify-center">
      <div
        class="background-color-square w-full md:mt-40 w-full md:ml-20 md:mr-20 ml-10 mr-10 mt-32"
      >
        <div class="flex justify-center mr-4 ml-4 md:mr-20 md:ml-20">
          <div class="text-white mt-10 mb-10">
            <nuxt-content :document="blog"></nuxt-content>
          </div>
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
  async asyncData({ $content, params }) {
    let blog = await $content("blogs/" + params.id).fetch();
    return {
      blog,
    };
  },
};
</script>

<style></style>
