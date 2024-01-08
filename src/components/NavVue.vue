<template>

    <nav class="flex justify-between h-[10vh]">

        <div class="flex w-[45vw] h-full items-center justify-evenly sm:w-[20%]">
          <img src="../assets/icon-menu.svg" class="ml-10 sm:hidden">
          <img src="../assets/logo.svg" class="ml-2">
        </div>

        <div id="nav_medio" class="hidden sm:flex sm:items-center sm:justify-start sm:w-[60%]">
          <div class="sm:flex sm:justify-between sm:w-[50%]">
            <router-link to="/collection" class="subrayar">Collections</router-link>
            <router-link to="/" class="subrayar">Men</router-link>
            <router-link to="/" class="subrayar">Women</router-link>
            <router-link to="/about" class="subrayar">About</router-link>
            <router-link to="/contact" class="subrayar">Contact</router-link>
          </div>
        </div>

        <div class="flex w-[40%] h-full items-center justify-evenly sm:w-[20%]">
          <div>
            <!-- <div>
              <img src="../assets/icon-cart.svg" class="cursor-pointer" @click="mostrarCarro">
            </div> -->
            <div class="relative w-[32px] h-[23px] pr-6">
              <img src="../assets/icon-cart.svg" class="cursor-pointer absolute" @click="mostrarCarro">
              <span class="absolute top-[-7px] right-0 bg-[#ff7d1a] text-sm text-white rounded-full pl-[2px] pr-[2px]">0</span>
            </div>
            <div id="icon_num_prods" class="bg-[#ff7d1a]">
              <p>3</p>
            </div>
          </div>
          <img src="../assets/image-avatar.png" class="h-[50%] border border-2 border-[#ff7d1a] rounded-full cursor-pointer">
        </div>

    </nav>

</template>

<script>

export default {
  name: 'NavVue',
}
</script>

<style lang="sass" scoped>
    #icon_num_prods
        display: none
    .subrayar:hover
      text-decoration: underline
      text-decoration-color: #ff7d1a
      text-decoration-thickness: 0.2em // grosor del subrayado, em = 20% del tamaño de la fuente
      text-underline-offset: 0.6em // posición del subrayado, em = 60% del tamaño de la fuente
      
</style>