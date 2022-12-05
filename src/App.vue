<script setup lang="ts">
  import Header from "./components/Header.vue";
  import Footer from "./components/Footer.vue";

  let org = {
    projects: [
      {
        url: '#',
        banner: 'https://metatags.io/assets/meta-tags-16a33a6a8531e519cc0936fbba0ad904e52d35f34a46c97a2c9f6f7dd7d336f2.png',
        name: 'eArchives',
        descripton: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci ex quos qui sit dolore odio, tempore nesciunt aperiam, dolores voluptas nisi hic beatae. Iusto, quae cum cupiditate quod iure et?',
        tags: [ { color: '#235A97', text: 'Typescript' }, { color: '#41B983', text: 'Vue' }, { color: '#38bdf8', text: 'Tailwind' } ]
      }
    ],
    members: [
      {
        icon: 'https://i.imgur.com/UYYFkDS.jpg',
        name: 'Jürgen',
        role: 'Manager'
      },
      {
        icon: 'https://avatars.githubusercontent.com/u/70984139',
        name: 'Gregori',
        role: 'Developer'
      }
    ]
  }
  
</script>

<template>

  <header class="container mx-auto">
    <Header></Header>
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
          <a v-for="(project, index) in org.projects" v-bind:key="index" :href="project.url">
            <div class="bg-[#1d1d1d] p-2 rounded-lg hover:opacity-75 transition-opacity duration-300" >
              <img class="rounded-lg" :src="project.banner">
              <div class="px-2 py-4">
                <span class="text-xl">
                  <span v-html="project.name"></span> <i class="fa-solid fa-link text-sm opacity-25"></i>
                </span>

                <div class="py-4 text-sm">
                  <span v-for="(tag, i) in project.tags" class="rounded-full py-0.5 px-3 ml-2" :class="`bg-[${tag.color}]`" v-bind:key="i">{{ tag.text }}</span>
                </div>

                <p class="opacity-70">{{ project.descripton }}</p>
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
            <span class="text-lg text-accent font-semibold">Membros</span>
            <div class="grid grid-cols-4 mt-2">
              <div v-for="(m, i) in org.members" v-bind:key="i" class="w-32 text-center outline-2 outline-dashed outline-[#292929] rounded-lg p-2">
                <img :src="m.icon" class="rounded-full w-12 h-12 object-cover inline-block"/>
                <span class="text-base block mt-1">{{ m.name }}</span>
                <span class="text-sm bg-[#292929] px-2 py-0.5 rounded-full block mt-1">{{ m.role }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div id="features" class="bg-[#292929]">
      <div class="container mx-auto p-8">
        <h1 class="text-4xl text-white text-right">Statistics</h1>

        <section class="mb-32 text-center">
          <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-x-6 lg:gap-x-0 items-center">

            <div class="mb-12 lg:mb-0 relative">
              
              <h5 class="text-lg mb-4">1+</h5>
              <h6 class="font-medium">Lines of Code</h6>
              
            </div>

            <div class="mb-12 lg:mb-0 relative">
              
              <h5 class="text-lg font-medium mb-4">12+</h5>
              <h6 class="font-medium">Collaboratos</h6>
              
            </div>

            <div class="mb-12 md:mb-0 relative">
              
              <h5 class="text-lg mb-4">100+</h5>
              <h6 class="font-medium">Projects</h6>
              
            </div>

            <div class="relative">
              
              <h5 class="text-lg mb-4">3+</h5>
              <h6 class="font-medium mb-0">Languages</h6>
            </div>
          </div>
        </section>
      </div>
    </div>

    <div id="contact" class="h-96 bg-[#292929]">

    </div>

  </main>

  <footer>
    <Footer/>
  </footer>
</template>