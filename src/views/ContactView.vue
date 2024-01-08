<template>
    <div>
      <nav-vue></nav-vue>

      <div>
        <h1 class="border text-center text-2xl pt-6 pb-6 mb-4">Contact</h1>
        <div class="h-[65vh] pl-24 pr-24 flex flex-col items-center justify-evenly">
            <div class="border border-orange-200 rounded w-[30%] p-4 bg-[#f7f8fd]"><img src="../assets/logo.svg"></div>
            <div class="border border-orange-200 rounded w-[30%] p-4 bg-[#f7f8fd]">
                <p><i class="fa-solid fa-phone mr-4 text-[#ff7d1a]"></i>Teléfono: 123-456-7890</p>
            </div>
            <div class="border border-orange-200 rounded w-[30%] p-4 bg-[#f7f8fd]">
                <p><i class="fa-solid fa-envelope mr-4 text-[#ff7d1a]"></i>Email: info@sneakersco.com</p>
            </div>
            <div class="border border-orange-200 rounded w-[30%] p-4 bg-[#f7f8fd]">
                <p><i class="fa-brands fa-instagram mr-4 text-[#ff7d1a]"></i>Instagram: @sneakersco</p>
            </div>
            <div class="border border-orange-200 rounded w-[30%] p-4 bg-[#f7f8fd]">
                <p><i class="fa-solid fa-map-location-dot mr-4 text-[#ff7d1a]"></i>Ciudad: SneakerCity</p>
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

<style>

</style>