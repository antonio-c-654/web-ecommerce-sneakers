<template>

    <div id="menu_hamburguesa" class="h-screen w-[70vw] h-full pl-6 pt-4 font-bold sm:hidden">
      <img src="../assets/icon-close.svg">
      <br>
      <router-link to="/collection" class="subrayar">Collections</router-link> <br>
      <router-link to="/" class="subrayar">Men</router-link> <br>
      <router-link to="/" class="subrayar">Women</router-link> <br>
      <router-link to="/about" class="subrayar">About</router-link> <br>
      <router-link to="/contact" class="subrayar">Contact</router-link> <br>
      
    </div>
    
</template>

<script>
export default {
    name: 'MenuHamVue'
}
</script>

<style lang="sass" scoped>
  #menu_hamburguesa
    display: none
</style>