<template>
  <section>
    <nav class="bg-white px-6 py-4 border-b">
      <div class="flex items-center justify-between flex-wrap container mx-auto">
        <a href="/" class="flex items-center flex-no-shrink text-red mr-6 no-underline">
          <span class="font-semibold text-2xl text-shadow tracking-tight">Linda TV</span>
        </a>
        <div class="flex items-center w-auto ml-auto">
          <div class="text-sm flex-grow">
            <a href="#" class="hidden md:inline-block mt-0 inline-block text-black mr-4 no-underline">由罗伟伦制作</a>
          </div>
        </div>
        <div class="md:hidden">
          <button class="rounded-full h-8 w-8 flex items-center justify-center border border-grey-dark text-grey-dark" @click="menu = !menu"> <!-- v-on-clickaway="closeMenu" -->
            <!--<svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>-->

            <i class="fas fa-info"></i>
          </button>
        </div>
      </div>
    </nav>
    <ul class="text-center bg-white list-reset py-2 border-b" v-show="menu" >
      <li class="py-2"><a href="#" class="md:inline-block mt-0 inline-block text-black no-underline">由罗伟伦制作</a></li>
    </ul>
  </section>
</template>

<script>
  export default {
    data: function() {
      return {
        menu: false
      }
    },
    methods: {
      closeMenu: function() {
        this.menu = false
      }
    }
  }
</script>