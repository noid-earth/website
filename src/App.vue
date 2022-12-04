<script setup lang="ts">
  import Header from "./components/Header.vue";
  import Footer from "./components/Footer.vue";
</script>

<template>

  <header class="container mx-auto">
    <Header/>
  </header>

  <main>
    
    <div id="" class="h-96 container mx-auto px-4 mt-6">
      <h1 class="text-4xl text-white">A programming organization</h1>
        <p class="w-1/2 opacity-70">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestiae sint impedit modi excepturi sequi ducimus. Aut maxime eligendi fugiat porro itaque voluptatum corrupti voluptate ducimus laudantium, quibusdam officia praesentium eum velit doloribus? Quas maiores fuga nesciunt!</p>
    </div>

    <div id="projects" class="h-96 bg-[#292929]">

    </div>

    <div id="about" class="h-96 container mx-auto">

    </div>

    <div id="contact" class="h-96 bg-[#292929]">

    </div>

  </main>

  <footer>
    <Footer/>
  </footer>
</template>