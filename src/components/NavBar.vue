<template>
  <div class="fixed z-50 w-full bg-stone-800 py-2 px-2 flex items-center gap-4 justify-between bg-opacity-80 backdrop-blur">
    <a href="tel:0455083696" class="font-bold text-orange-300 text-lg">0455 083 696</a>
    <div class="flex gap-4 items-center">
      <a href="" class="nav-link">Home</a>
      <a href="" class="nav-link">Contact</a>
      <a href="" class="nav-link">News & Updates</a>
      <button class="px-5 py-3 text-base font-medium leading-6 text-white transition-colors duration-150 ease-in-out rounded-md focus:outline-none bg-gradient-to-tr from-orange-300 to-orange-500 hover:from-orange-100 hover:to-orange-500">Book Now</button>
    </div>
    
  </div>
</template>

<script>
export default {

}
</script>

<style lang="postcss">
.nav-link {
  @apply text-orange-300
}

.nav-link:hover {
  @apply text-orange-100
}
</style>