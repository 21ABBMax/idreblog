<template>
  <div>
    <div class="min-h-screen flex justify-center">
      <div
        class="background-color-square md:mt-40 w-full md:ml-20 md:mr-20 ml-10 mr-10 mt-32"
      >
        <div class="text-white mt-32 flex flex-col">
          <h1 class="text-4xl flex justify-center text-center">
            Summer and Autumn Collection
          </h1>
          <p class="text-center mt-8 italic underline">
            Please choose the blog you want to read below
          </p>
          <div
            class="flex flex-wrap"
            style="justify-content: center; margin-bottom: 200px"
          >
            <div
              @click="goToBlog(page.id)"
              class="w-56 m-6 h-full"
              style="cursor: pointer"
              v-for="page in blogs"
              :key="page.id"
            >
              <PostItemComponent :item="page"></PostItemComponent>
            </div>
          </div>
        </div>
        <div class="flex justify-center mb-20">
          <h3 class="text-white italic text-lg animate-pulse">
            More comming soon!
          </h3>
        </div>
      </div>
    </div>
    <FooterComp />
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    let blogs = await $content("blogs").without(["body"]).fetch();
    console.log(blogs);
    blogs = blogs.filter(function (page) {
      console.log(page.theme);
      if (page.theme === "summer") return true;
      return false;
    });

    return {
      blogs,
    };
  },
  methods: {
    goToBlog(id) {
      this.$router.push("/blog-details/" + id);
    },
  },
};
</script>

<style></style>
