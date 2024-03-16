<script setup></script>

<template>
  <nav class="bg-sky-950">
    <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
      <div class="relative flex items-center justify-between h-16">
        <div class="hidden sm:block sm:ml-6">
          <div class="flex space-x-4">
            <!--Home tab-->
            <NuxtLink
              to="/"
              :class="{ 'text-white': $route.path === '/' }"
              class="text-gray-300 hover:bg-sky-600 px-3 py-2 rounded-md text-sm font-medium"
            >
              Home
            </NuxtLink>

            <!--About tab-->
            <NuxtLink
              to="/about"
              :class="{ 'text-white': $route.path === '/about' }"
              class="text-gray-300 hover:bg-sky-600 hover:text-white px-3 py-2 rounded-md text-sm font-medium"
            >
              About
            </NuxtLink>

            <!--Contact tab-->
            <NuxtLink
              to="/contact"
              :class="{ 'text-white': $route.path === '/contact' }"
              class="text-gray-300 hover:bg-sky-600 hover:text-white px-3 py-2 rounded-md text-sm font-medium"
            >
              Contact us
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<style lang="css" scoped></style>
