<template>
  <header class="sm:flex sm:justify-between sm:items-center sm:px-4 sm:py-3 px-2 py-2 border_bottom">
    <div class="flex items-center justify-between px-1 py-1 sm:px-4 sm:py-2">
      <div class="pointer logo_font">
        <nuxt-link to="/" class="text-2xl sm:text-3xl tracking-tight">
          Stempro
          <span class="text-gray-500">Solutions</span>
        </nuxt-link>
      </div>
      <div class="sm:hidden">
        <button @click="isOpen = !isOpen" type="button" class="block text-gray-500 focus:outline-none">
          <svg class="h-6 w-6 fill-current" viewBox="0 0 24 24">
            <path v-if="isOpen" fill-rule="evenodd" d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1 1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828 4.829 4.828 4.828z"/>
            <path v-if="!isOpen" fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"/>
          </svg>
        </button>
      </div>
    </div>
    <nav :class="isOpen ? 'block' : 'hidden'" class="px-4 pt-2 pb-4 sm:flex">
      <nuxt-link to="/" @click.native="isOpen = !isOpen" class="mt-1 block px-3 py-1 font-semibold rounded sm:mt-0 sm:ml-2">Home</nuxt-link>
      <nuxt-link to="/" @click.native="isOpen = !isOpen" class="mt-1 block px-3 py-1 font-semibold rounded sm:mt-0 sm:ml-2">Services</nuxt-link>
      <nuxt-link to="/" @click.native="isOpen = !isOpen" class="mt-1 block px-3 py-1 font-semibold rounded sm:mt-0 sm:ml-2">Company</nuxt-link>
      <nuxt-link to="/contact" @click.native="isOpen = !isOpen" class="mt-1 block px-3 py-1 font-semibold rounded sm:mt-0 sm:ml-2">Contact</nuxt-link>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    }
  },
}
</script>
<style>
.font_size_xl {
    font-size: 1.5rem;
}
.pointer {
    cursor: pointer;
}
.logo_font {
  font-family: 'Baloo Chettan 2' !important;
}

.border_bottom {
  border-bottom: 1px solid #ffffff;
}
</style>
