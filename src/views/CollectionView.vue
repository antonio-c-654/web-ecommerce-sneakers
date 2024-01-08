<template>
  <div>
    <nav-vue></nav-vue>
    <div>
      <h1 class="border text-center text-2xl pt-8 pb-6 mb-4">Collections</h1>
      <!-- <div class="clase1 flex justify-evenly">
        <img src="../assets/image-product-3.jpg">
        <img src="../assets/image-product-4.jpg">
      </div> -->
      <div class="clase1 flex justify-evenly">
        <div class="w-[300px] h-[300px] flex items-end justify-center cursor-pointer">
          <img src="../assets/image-product-3.jpg" class="absolute"> <span class="relative border border-black w-full text-center pt-2 pb-2 text-2xl bg-[#f7f8fd] rounded-b-2xl">Invierno</span>
        </div>
        <div class="w-[300px] h-[300px] flex items-end justify-center cursor-pointer">
          <img src="../assets/image-product-4.jpg" class="absolute"> <span class="relative border border-black w-full text-center pt-2 pb-2 text-2xl bg-[#f7f8fd] rounded-b-2xl">Otoño</span>
        </div>
        
        
      </div>
    </div>
    
  </div>
</template>

<script>
import NavVue from '../components/NavVue.vue'
export default {
  components: { NavVue },

}
</script>

<style lang="sass" scoped>
  .clase1 img
    width: 300px
    border: 2px solid black
    border-radius: 20px
    opacity: 0.7
  .clase1 img:hover
    opacity: 1
    

</style>
