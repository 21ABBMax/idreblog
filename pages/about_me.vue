<template>
  <div>
    <div class="min-h-screen pt-36 mr-10 ml-10 md:pt-40 md:mr-20 md:ml-20">
      <div class="background-color-square min-h-screen">
        <div class="flex justify-center flex-col items-center">
          <div class="mt-16">
            <h1
              class="text-yellow-200 italic text-bold text-4xl animate-bounce"
            >
              About me
            </h1>
          </div>
          <div class="flex justify-center mt-10 md:mt-0">
            <img
              class="h-3/4 w-3/4 md:w-full md:h-full md:mt-10 border-4 border-yellow-200"
              src="/images/Me.jpg"
            />
          </div>
          <div class="flex justify-center mr-4 ml-4 md:mr-20 md:ml-20">
            <div class="text-white mt-10 mb-10 transition-color">
              <nuxt-content :document="aboutInfo"></nuxt-content>
            </div>
          </div>
        </div>
      </div>
    </div>
    <FooterComp />
  </div>
</template>

<style>
.Underline {
  text-decoration-color: rgb(253, 230, 138);
}

#MarginStyle1 {
  margin-left: 5%;
  margin-right: 5%;
}

#MarginStyle2 {
  margin-top: 5%;
}

#MarginStyle3 {
  margin-left: 5%;
}
</style>
<script>
export default {
  async asyncData({ $content }) {
    let aboutInfo = await $content("/blogs/About-Me").fetch();

    return {
      aboutInfo,
    };
  },
};
</script>
