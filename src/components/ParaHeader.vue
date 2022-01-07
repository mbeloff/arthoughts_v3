<template>
  <div data-jarallax class="jarallax header relative">
      <div class="absolute h-full w-full bg-stone-900/30 grid items-center py-50 px-2">
        <div class="header-content container mx-auto h-2/3 grid grid-cols-1 md:grid-cols-2">
          <div class="p-8 bg-white/10 backdrop-blur-sm span-full md:span-1 rounded-2xl">
            <img src="https://ik.imagekit.io/y3ayiqneqlr/assets/discover-jop.svg" alt="Discover the Joy of Painting in cursive text" class="droppy">
            <p class="text-2xl md:text-4xl font-medium text-white droppy">
              Painting workshops with Maaret Webb, teaching artist and Certified Bob Ross Instructor
            </p>
            <button class="mt-4 text-xl text-white border-white border rounded px-4 py-2 hover:shadow-lg shadow-blue-800/30">Book Now</button>
          </div>
        </div>
      </div>
      <img ref="bg-img" class="jarallax-img bg-fixed" :src="backgroundimage" alt="">
  </div>
</template>

<script>
  import 'object-fit-images'
  import { jarallax, jarallaxVideo } from 'jarallax';
  export default {
data() {
      return {
        backgroundimage: ""
      }
    },
    mounted() {
      this.grabImage()
      jarallaxVideo();
      jarallax(document.querySelectorAll('.jarallax'), {
        speed: 0.5
      })
      
    },
    computed: {
    },
    methods: {
      grabImage() {
        let url = 'https://ik.imagekit.io/y3ayiqneqlr/headers/' + (Math.floor(Math.random() * 12) + 1) + '.jpg'     
        console.log(url) 
        this.backgroundimage = url
        }
    }
  }
</script>

<style>
.jarallax {
    position: relative;
    z-index: 0;
  }

  .jarallax>.jarallax-img {
    position: absolute;
    object-fit: cover;
    /* support for plugin https://github.com/bfred-it/object-fit-images */
    font-family: 'object-fit: cover;';
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
  }

  .header {
    height: 50vh;
    min-height: 700px;
  }

  .header-content {
    margin-top: 64px

  }

  .droppy {
    filter: drop-shadow( 3px 3px 2px rgba(0, 0, 0, .7))
  }
</style>