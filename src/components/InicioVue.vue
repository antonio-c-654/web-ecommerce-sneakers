<template>
  <div id="inicio_principal">
    
    <nav-vue class="border-b-[1px]"></nav-vue>
    <menu-hamb-vue></menu-hamb-vue>


    <div id="carrito" class="hidden w-[96vw] h-[35vh] bg-white rounded-lg mt-2 p-4 absolute left-1/2 transform -translate-x-1/2 sm:w-[30vw] sm:ml-80 sm:border sm:border-black-200">
        <div class="w-full border-b border-gray-400 text-sm pb-2">
          <p><strong>Cart</strong></p>
        </div>

        <div id="contenido_cart" class="flex flex-col items-center justify-center mt-2 h-[80%]">

          <!-- default vacio -->
          <!-- <p class="text-sm text-[#68707d]">Your cart is empty.</p> -->

          <div class="producto flex items-center justify-between w-full text-xs text-[#68707d]">
            
            <div class="h-[40px]">
              <img src="../assets/image-product-1-thumbnail.jpg" class="h-full rounded-sm">
            </div>
            <div class="h-full flex flex-col justify-between">
              <p>Fall Limited Edition Sneakers</p>
              <p>
                <span id="precio_prod">$125.00</span> x 
                <span id="cantidad_prod">3</span> 
                <strong id="precio_total" class="text-black pl-4">$375.00</strong>
              </p>
            </div>
            <i class="fa-regular fa-trash-can"></i>
          </div>

          <button class="bg-[#ff7d1a] text-white rounded-lg h-12 w-[90vw] mt-4 sm:w-[90%]">Checkout</button>

        </div>

    </div>


    <div id="resto" class="sm:flex sm:justify-evenly sm:h-[90vh] sm:pt-16">

    <div id="div_imagen" class="h-[40vh] w-screen flex items-center justify-between pl-4 pr-4 bg-red-500 sm:bg-green-500 bg-cover bg-center sm:w-[40%] sm:h-[70%] imag1">
      <i class="fa-solid fa-angle-left h-[20px] w-[20px] border rounded-full p-4 bg-white flex items-center justify-center font-bold cursor-pointer" @click="restaurarImagen"></i>
      <i class="fa-solid fa-angle-right h-[20px] w-[20px] border rounded-full p-4 bg-white flex items-center justify-center font-bold cursor-pointer" @click="cambiarImagen"></i>
      <!-- <img src="../assets/image-product-1.jpg" alt=""> -->
      <!-- bg-[url('../assets/image-product-1.jpg')] -->
    </div>
  
    
    <div id="descripcion" class="pl-4 pr-4 w-full flex flex-col pb-12 sm:w-[30%] sm:h-[80%]">
        <h3 class="text-[#ff7d1a] text-sm uppercase font-bold mt-4">Sneaker Company</h3>
        <h1 class="text-2xl font-bold mt-2 sm:text-3xl">Fall Limited Edition Sneakers</h1>
        <p class="text-sm text-[#68707d] mt-4">These low-profile sneakers are your perfect casual wear companion. Featuring a durable rubber outer sole, they'll withstand everything the weather can offer.</p>
        
        <div class="flex justify-between mt-4">
          <div class="flex">
            <p class="text-2xl font-bold">$125.00</p>
            <p class="text-[#ff7d1a] bg-[#ffede0] font-bold ml-4 pl-2 pr-2 flex items-center">50%</p>
          </div>
          <p class="text-[#68707d] sm:hidden">$250.00</p>
        </div>
        <p class="text-[#68707d] hidden sm:block">$250.00</p>
        
        
        <div id="nose" class="sm:flex sm:justify-between">
        <div class="h-12 rounded-lg flex justify-between items-center bg-[#f7f8fd] pl-6 pr-6 sm:pl-4 sm:pr-4 mt-4 sm:w-[35%]">
          <button class="text-[#ff7d1a] text-2xl font-bold" @click="disminuirCant">-</button>
          <!-- <input type="number" placeholder="0" class="w-[45px] text-center bg-[#f7f8fd]"> -->
          <p id="cantidad_prod">{{ cantidad }}</p>
          <button class="text-[#ff7d1a] text-2xl font-bold" @click="aumentarCant">+</button>
        </div>
      
        <button class="bg-[#ff7d1a] text-white rounded-lg h-12 w-[90vw] mt-4 sm:w-[60%]" @click="comprarPopUp">
          <i class="fa-solid fa-cart-shopping mr-4"></i>Add to cart
        </button>
        </div>
      </div>

    </div>


  </div>
</template>

<script>
import MenuHambVue from './MenuHambVue.vue'
import NavVue from './NavVue.vue'
export default {
  components: { NavVue, MenuHambVue },
  name: 'InicioVue',
  data(){
    return{
      cantidad: 0,
    }
  },
  methods: {
    mostrarCarro(){
      let carro = document.getElementById('carrito')
      carro.classList.toggle("hidden")
    },
    cambiarImagen(){
      let div_imagen = document.getElementById('div_imagen')
      div_imagen.classList.toggle("imag1")
      div_imagen.classList.toggle("imag2")
    },
    restaurarImagen(){
      let div_imagen = document.getElementById('div_imagen')
      div_imagen.classList.toggle("imag1")
      div_imagen.classList.toggle("imag2")
    },
    aumentarCant(){
      this.cantidad += 1
    },
    disminuirCant(){
      if(this.cantidad<=0){
        this.cantidad = 0
      }
      else{
        this.cantidad -= 1
      }
    }
    // ,
    // comprarBot(){
    //   Swal.fire({
    //     position: "top-center",
    //     icon: "success",
    //     title: "Añadido al carrito",
    //     showConfirmButton: false,
    //     timer: 1500
    //   })
    // }

  }
}
</script>

<style lang="sass" scoped>
  // #div_imagen
  //   background-image: url('../assets/image-product-1.jpg')
  .imag1
    background-image: url('../assets/image-product-1.jpg')
  .imag2
    background-image: url('../assets/image-product-4.jpg')
</style>