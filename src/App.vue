<script setup lang="ts">
  import Header from "./components/Header.vue";
  import Footer from "./components/Footer.vue";
  //@ts-ignore
  import Adsense from "./components/Adsense.vue";

  import org from "./data";
  
</script>

<template>

  <header class="container mx-auto">
    <Header></Header>
  </header>

  <main>
    
    <div id="" class="container mx-auto px-4 mt-8 pb-40">
      <h1 class="text-4xl text-white">Welcome!</h1>
      <p class="text-lg w-full md:w-2/3 opacity-70 py-2 block">We are a group of enthusiastic developers creating innovative, creative and fun projects.</p>
    </div>

    <div id="projects" class="bg-[#292929]">
      <div class="container mx-auto p-8 pb-20">
        <h1 class="text-4xl text-white text-center md:text-right">Projects</h1>

        <div class="grid grid-cols-1 lg:grid-cols-2 2xl:grid-cols-4 gap-2 md:gap-4 mt-6 rounded-lg pb-12">
          <a v-for="(project, index) in org.projects" v-bind:key="index" :href="project.url" target="_blank" rel="noopener noreferrer">

            <div class="bg-[#1d1d1d] p-2 rounded-lg hover:opacity-75 transition-opacity duration-300 ring-1 ring-neutral-700/50">
              <img class="rounded-lg" :src="(project.banner.length > 5) ? project.banner : '/images/banner.png'">
              <div class="px-2 py-4">
                <span class="text-xl">
                  <span v-html="project.name"></span> <i class="fa-solid fa-link text-sm opacity-25"></i>
                </span>

                <div class="py-4 text-sm">
                  <span v-for="(tag, i) in project.tags" class="rounded-full py-0.5 px-3 mr-2 bg-[#292929] ring-1 ring-neutral-700/50" v-bind:key="i">{{ tag.text }}</span>
                </div>

                <p class="opacity-70">{{ project.descripton }}</p>
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>

    <div id="links" class="">
      <div class="container mx-auto p-8 md:pb-20">
        <h1 class="text-4xl text-white text-center md:text-left">Contact</h1>

        <div class="grid md:grid-cols-3 py-4 mt-6 pb-20">
          <div>
            <h1 class="text-lg">Get in touch with us</h1>
            
            <ul>
              <li class="py-2">
                <a href="mailto:contact@projectdema.com" class="font-semibold">
                  <i class="fa-solid fa-envelope opacity-50"></i> <span class="px-2 text-accent">contact@noid.earth</span>
                </a>
              </li>
              <li class="py-2">
                <a href="https://discord.gg/GtaxXxNYaD" class="font-semibold" target="_blank" rel="noopener noreferrer">
                  <i class="fa-brands fa-discord opacity-50"></i> <span class="px-2 text-accent">Chat with us</span>
                </a>
              </li>
            </ul>
          </div>
          <div>
            <h1 class="text-lg mt-4 md:mt-0">Social</h1>

            <ul>
              <li class="py-2">
                <a href="https://github.com/noid-earth" class="font-semibold" target="_blank" rel="noopener noreferrer">
                  <i class="fa-brands fa-github opacity-50"></i> <span class="px-2 text-accent">Github</span>
                </a>
              </li>

              <li class="py-2">
                <a href="https://instagram.com/noid-earth" class="font-semibold" target="_blank" rel="noopener noreferrer">
                  <i class="fa-brands fa-instagram opacity-50"></i> <span class="px-2 text-accent">Instagram</span>
                </a>
              </li>

              <li class="py-2">
                <a href="https://twitter.com/noid-earth" class="font-semibold" target="_blank" rel="noopener noreferrer">
                  <i class="fa-brands fa-twitter opacity-50"></i> <span class="px-2 text-accent">Twitter</span>
                </a>
              </li>
            </ul>
            
          </div>
          <div>
            <Adsense/>
          </div>
        </div>
      </div>
    </div>

  </main>

  <footer>
    <Footer/>
  </footer>
</template>