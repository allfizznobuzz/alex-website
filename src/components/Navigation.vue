<script>
export default {
  data() {
    return {
      mobile: false,
    }
  },
}
</script>

<template>
  <nav bg-gray-100>
    <div class="max-w-6x1 mx-auto px-4">
      <div flex justify-between>
        <div flex>
          <!-- logo -->
          <div class="mr-4">
            <a href="#" flex items-center class="py-5 px-2 text-gray-700">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-1 text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
              <span class="font-bold">Legal Nursing</span>
            </a>
          </div>
          <!-- primary nav -->
          <div class="hidden md:flex items-center space-x-1">
            <a href="" class="py-5 px-2 text-gray-700 hover:text-gray-900">Features</a>
            <a href="" class="py-5 px-2 text-gray-700 hover:text-gray-900">Pricing</a>
          </div>
        </div>
        <!-- secondary nav -->
        <div class="hidden md:flex items-center space-x-1">
          <a href="" class="py-5 px-3">Login</a>
          <a
            href="" class="py-2 px-3 bg-yellow-400 hover:bg-yellow-300 text-yellow-900 hover:text-yellow-800
          rounded transition duration-300"
          >Signup</a>
        </div>
        <!-- mobile button -->
        <div class="md:hidden flex items-center">
          <button @click="mobile = !mobile">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
        </div>
      </div>
    </div>
    <!-- mobile menu -->
    <div
      v-if="mobile" class="md:hidden absolute"
    >
      <a href="#" class="block py-2 px-4 text-sm hover:bg-gray-200">Features</a>
      <a href="#" class="block py-2 px-4 text-sm hover:bg-gray-200">Pricing</a>
    </div>
  </nav>
</template>
