<template>
    <header role="banner" class="flex justify-between items-center h-[10vh] bg-blue-50 px-4 md:px-10">
      <div >
        <router-link to="/" >
          logo
        </router-link>
      </div>
    
      <nav role="navigation" class="flex md:justify-between">
        <ul role="menu" class="flex  items-center   gap-7 font-semibold text-[18px] flex-col md:flex-row absolute md:static md:h-auto bg-blue-50 w-full left-[-100%] h-[100dvh] transition-all top-0 justify-center"
            :class="{ show: showMenu }">
          <span tabindex="0" @click="menuToggle" @keydown.enter="menuToggle"
                class="md:hidden absolute top-7 right-[5%] w-6 h-6 cursor-pointer opacity-0 transition-opacity"
                :class="{showContact : showMenu}">
                <img src="../assets/close.png" alt="Close" class="w-full h-full" />
          </span>
          <li role="menu item"><a href="#"  @click="menuToggle">Home</a></li>
          <li role="menu item"><a href="#about"  @click="menuToggle">About</a></li>
          <li role="menu item"><a href=""  @click="menuToggle">Portfolio</a></li>
        </ul>
      </nav>
    
      <div class="absolute md:static border-2 border-blue-300 rounded-md md:h-auto md:w-auto w-full left-0 top-[33rem] md:top-0 flex items-end justify-center opacity-0 md:opacity-100 transition-opacity"
            :class="{showContact : showMenu}">
        <button aria-label="Contact" class="text-black font-semibold md:px-7  linear py-2 px-5 rounded-md">Contact</button>
      </div>
    
      <button aria-label="Toggle Menu" aria-haspopup="true" class="md:hidden flex cursor-pointer" @click="menuToggle" @keyup.enter="menuToggle">
        <img src="../assets/hamburger.png" alt="Menu" class="w-8 h-8 aspect-square" />
      </button>
    </header>
    
    </template>
    <script setup>
    import { ref } from "vue";
    
    const showMenu = ref(false);
    const menuToggle = () => {
      showMenu.value = !showMenu.value;
      console.log(showMenu.value);
    };
    </script>
    <style scoped>
   
    .router-link-exact-active {
      /* border-bottom: 2px solid #D45800; */
      color: #4000d4;
    }
    .show {
      /* transform: translateX(100%); */
      left: 0;
      transition: 0.2s all;
    }
    .showContact{
      opacity:1;
      transition: opacity 1s linear;
    }
    </style>
    