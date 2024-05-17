<template>
  <header>
    <nav class="bg-teal-500 border-gray-200 px-4 lg:px-6 py-2.5 dark:bg-blue-900">
      <div class="flex flex-wrap justify-between items-center mx-auto max-w-screen-xl">
        <a href="https://flowbite.com" class="flex items-center">
          <img src="~/assets/images/shirt.svg" class="mr-3 h-6 sm:h-9" alt="Flowbite Logo" />
          <span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white">
            APLIKASI GUDANG
          </span>
        </a>
       
        <div>
          <ul class="flex flex-col mt-4 font-medium lg:flex-row lg:space-x-8 lg:mt-0">
            <li>
              <a href="/" class="block py-2 pr-4 pl-3 text-black-700 rounded bg-primary-700 lg:bg-transparent lg:text-primary-700 lg:p-0 dark:text-white" aria-current="page">
                Home
              </a>
            </li>
            <li>
              <a href="/kategori" class="block py-2 pr-4 pl-3 text-black border-b border-gray-100 hover:bg-gray-50 lg:hover:bg-transparent lg:border-0 lg:hover:text-primary-700 lg:p-0 dark:text-gray-400 lg:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white lg:dark:hover:bg-transparent dark:border-gray-700">
                Kategori
              </a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
  <slot />
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped></style>
