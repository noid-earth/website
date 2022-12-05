<template>
    <nav class="py-2.5 rounded-lg">
      <div class="flex flex-wrap items-center justify-between">

        <a href="/">
          <span class="text-xl font-semibold ml-4">project<span class="text-accent">Dema</span></span>
        </a>

        <button data-collapse-toggle="navbar" type="button" class="inline-flex items-center p-2 ml-3 text-sm rounded-lg md:hidden" aria-controls="navbar" aria-expanded="false">
          <span class="sr-only">Open main menu</span>
          <i class="fa-solid fa-bars p-2"></i>
        </button>

        <div class="hidden w-full md:block md:w-auto" id="navbar">
          <ul class="flex flex-col p-4 mt-4 border bg-[#292929] rounded-lg md:m-0 m-4 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium md:border-0">
            <li>
              <a href="#" class="block py-2 pl-3 pr-4 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 md:hover:opacity-75">Home</a>
            </li>
            <li>
              <a href="#projects" class="block py-2 pl-3 pr-4 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 md:hover:opacity-75">Projects</a>
            </li>
            <li>
              <a href="#about" class="block py-2 pl-3 pr-4 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 md:hover:opacity-75">About</a>
            </li>
            <li>
              <a href="#statistics" class="block py-2 pl-3 pr-4 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 md:hover:opacity-75">Statistics</a>
            </li>
            <li>
              <a href="#contact" class="block py-2 pl-3 pr-4 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 md:hover:opacity-75">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
</template>

<script lang="ts">
export default {
  name: 'Header'  
}
</script>