<template>
  <div>
    <nav-bar></nav-bar>   
    <para-header></para-header>
      <router-view />

    <div class="h-screen"></div>
    <footer class="text-center py-4 bg-stone-700 text-stone-900">
      <p>&copy 2022 arthoughts.com</p>
    </footer>
  </div>
</template>

<script>
  import NavBar from '@/components/NavBar.vue'
  import ParaHeader from '@/components/ParaHeader.vue'
  export default {
    
    components: {
      NavBar, ParaHeader
    },
    
  }
</script>

<style>
</style>