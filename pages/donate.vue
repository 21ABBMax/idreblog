<template>
  <div>
    <div class="min-h-screen flex justify-center flex-col items-center">
      <div class="m-4 justify-center items-center">
        <h1 class="text-white text-xl mt-20">Feel free to donate!</h1>
      </div>
      <div class="mb-20">
        <p class="text-white italic text-sm md:text-normal mr-8 ml-8">
          If you find this site good, and you want to help out with future
          projects, you are free to leave a donation in any size!
        </p>
      </div>
      <p class="text-white text-sm italic mb-8">P.S! Only Swish!</p>
      <img class="rounded-md" id="SwishTag" src="/images/Min_Swish.png" />
    </div>
    <FooterComp />
  </div>
</template>
<style>
#SwishTag {
  height: auto;
  max-width: 50%;
  border: 4px solid rgb(255, 255, 255);
}
</style>
