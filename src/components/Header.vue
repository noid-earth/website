<template>
    <nav class="py-2.5 rounded-lg">
      <div class="flex flex-wrap items-center justify-between">

        <a href="/">
          <span class="text-xl font-semibold ml-4">project<span class="text-accent">Dema</span></span>
        </a>

        <div class="items-center justify-between w-auto flex">
          <ul class="flex flex-row p-4 mt-4 space-x-8">
            <li>
              <a href="#" class="">Home</a>
            </li>
            <li>
              <a href="#projects" class="">Projects</a>
            </li>
            <li>
              <a href="#about" class="">About</a>
            </li>
            <li>
              <a href="#contact" class="">Contact</a>
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