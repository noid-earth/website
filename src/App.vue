<script lang="ts">
  import Header from "./components/Header.vue";
  import Footer from "./components/Footer.vue";

  export default {
    data() {
      
    }
  }
</script>

<template>

  <header class="container mx-auto">
    <Header/>
  </header>

  <main>
    
    <div id="" class="h-96 container mx-auto px-4 mt-8">
      <h1 class="text-4xl text-white">A programming organization</h1>
      <p class="text-lg w-1/2 opacity-70 py-2 block">An organization created to bring code lovers together to create innovative, creative and fun projects.</p>
      <a href="#projects" class="px-6 py-2 mt-2 rounded-lg bg-accent inline-block">
        See more
      </a>
    </div>

    <div id="projects" class="bg-[#292929]">
      <div class="container mx-auto p-8">
        <h1 class="text-4xl text-white text-right">Projects</h1>

        <div class="grid grid-cols-4 gap-4 mt-6 rounded-lg">
          <a href="#">
            <div class="bg-[#1d1d1d] p-2 rounded-lg hover:opacity-75 transition-opacity duration-300">
              <img class="rounded-lg" src="https://metatags.io/assets/meta-tags-16a33a6a8531e519cc0936fbba0ad904e52d35f34a46c97a2c9f6f7dd7d336f2.png" alt="">
              <div class="px-2 py-4">
                <span class="text-xl">
                  eArchives <i class="fa-solid fa-link text-sm opacity-25"></i>
                </span>

                <div class="py-4 text-sm">
                  <span class="rounded-full bg-[#235A97] py-0.5 px-3">Typescript</span>
                  <span class="rounded-full bg-[#41B983] py-0.5 px-3 ml-2">Vue</span>
                  <span class="rounded-full bg-[#38bdf8] py-0.5 px-3 ml-2">Tailwind</span>
                </div>

                <p class="opacity-70">
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci ex quos qui sit dolore odio, tempore nesciunt aperiam, dolores voluptas nisi hic beatae. Iusto, quae cum cupiditate quod iure et?
                </p>
              </div>
            </div>
          </a>

          
        </div>
      </div>
    </div>

    <div id="about" class="">
      <div class="container mx-auto p-8">
        <h1 class="text-4xl text-white text-left">About</h1>

        <div class="grid grid-cols-2 gap-4">
          <div>

          </div>
          <div>
            <div class="grid grid-cols-4 gap-2">
              <img src="https://i.imgur.com/UYYFkDS.jpg" alt="">
            </div>
          </div>
        </div>
      </div>
    </div>

    <div id="contact" class="h-96 bg-[#292929]">

    </div>

  </main>

  <footer>
    <Footer/>
  </footer>
</template>