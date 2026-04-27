<template>
<div class="w-full relative h-[700px]">
    <!-- Red Section -->
  <img 
        src="../assets/Hospital.png" 
        alt="NovaCare Hospital"
        class="w-full h-full object-cover"
    >

    <!-- Optional Dark Overlay -->
    <div class="absolute inset-0 bg-black/30"></div>

    <!-- Optional Text -->
    <div class="absolute inset-0 flex items-center justify-center">
        <h1 class="text-white text-4xl font-bold drop-shadow-lg">
            NovaCare Hospital
        </h1>
    </div>


</div>
  <div class="flex justify-center gap-4 p-4 bg-gray-100">
    <docInfo src="DR1.png" />
    <docInfo src="DR2.png" />
    <docInfo src="DR3.png" />
    <docInfo src="DR4.png" />
  </div>

</template>
<script>
import img1 from "../assets/img1.jpg";
import img2 from "../assets/img2.webp";
import img3 from "../assets/img3.png";
import img4 from "../assets/img4.jpg";
import img5 from "../assets/img5.jpg";
import docInfo from "./docInfo.vue";

export default { 
  components: {
    docInfo,
  },
  data() {
    return {
      currentIndex: 0,
      images: [img1, img2, img3, img4, img5], // Array of image paths
    };
  },
  mounted() {
    this.startAutoSlide();
  },
  beforeUnmount() {
    clearInterval(this.interval); // Clear the interval when the component unmounts
  },
  methods: {
    startAutoSlide() {
      this.interval = setInterval(() => {
        this.currentIndex = (this.currentIndex + 1) % 2; // Loop back to the first slide
      }, 7000); // Change slide every 7 seconds
    },
  },

  name: 'LandingPage'

  
}
</script>