<script setup lang="ts">
  import Header from "./components/Header.vue";
  import Footer from "./components/Footer.vue";

  let org = {
    projects: [
      {
        url: 'https://github.com/projectdema/earchives',
        banner: '/eArchives/banner.png',
        name: 'eArchives',
        descripton: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci ex quos qui sit dolore odio, tempore nesciunt aperiam, dolores voluptas nisi hic beatae. Iusto, quae cum cupiditate quod iure et?',
        tags: [ { text: 'Typescript' }, { text: 'Vue' }, { text: 'Tailwind' } ]
      }
    ],
    members: [
      {
        icon: 'https://i.imgur.com/UYYFkDS.jpg',
        name: 'Jürgen',
        role: 'Manager',
        github: 'https://github.com/jurgenjacobsen',
      },
      {
        icon: 'https://avatars.githubusercontent.com/u/70984139',
        name: 'Gregori',
        role: 'Developer',
        github: '',
      }
    ],
    stats: [
      {
        title: 'Languages of Code',
        num: 7
      },
      {
        title: 'Lines of Code',
        num: 12128
      },
      {
        title: 'Collaboratos',
        num: 2
      },
      {
        title: 'Projects',
        num: 3
      }
    ]
  }
  
</script>

<template>

  <header class="container mx-auto">
    <Header></Header>
  </header>

  <main>
    
    <div id="" class="container mx-auto px-4 mt-8 pb-40">
      <h1 class="text-4xl text-white">A programming organization</h1>
      <p class="text-lg w-full md:w-1/2 opacity-70 py-2 block">An organization created to bring code lovers together to create innovative, creative and fun projects.</p>
      <a href="#projects" class="px-6 py-2 mt-2 rounded-lg bg-accent inline-block">
        See more
      </a>
    </div>

    <div id="projects" class="bg-[#292929]">
      <div class="container mx-auto p-8 pb-20">
        <h1 class="text-4xl text-white text-center md:text-right">Projects</h1>

        <div class="grid grid-cols-1 md:grid-cols-4 gap-2 md:gap-4 mt-6 rounded-lg pb-12">
          <a v-for="(project, index) in org.projects" v-bind:key="index" :href="project.url" target="_blank" rel="noopener noreferrer">

            <div class="bg-[#1d1d1d] p-2 rounded-lg hover:opacity-75 transition-opacity duration-300">
              <img class="rounded-lg" :src="(project.banner.length > 5) ? project.banner : '/images/banner.png'">
              <div class="px-2 py-4">
                <span class="text-xl">
                  <span v-html="project.name"></span> <i class="fa-solid fa-link text-sm opacity-25"></i>
                </span>

                <div class="py-4 text-sm">
                  <span v-for="(tag, i) in project.tags" class="rounded-full py-0.5 px-3 mr-2 bg-[#292929]" v-bind:key="i">{{ tag.text }}</span>
                </div>

                <p class="opacity-70">{{ project.descripton }}</p>
              </div>
            </div>
          </a>
        </div>
      </div>
    </div>

    <div id="about" class="">
      <div class="container mx-auto p-8 pb-20">
        <h1 class="text-4xl text-white text-center md:text-left">About</h1>

        <div class="grid md:grid-cols-2 md:gap-4">
          <div>
            <h1 class="text-lg text-accent">Why?</h1>
            <p class="opacity-70 md:w-4/5 mt-2">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Praesentium, distinctio, doloribus maiores commodi eius nostrum totam earum placeat obcaecati ipsa culpa quas accusantium laboriosam sequi molestiae sed animi molestias modi.
            </p>
          </div>
          <div>
            <h1 class="text-lg text-accent mt-4 md:mt-0">Members</h1>
            <div class="grid grid-cols-2 grid:grid-cols-4 gap-4 mt-2">
              <a v-for="(m, i) in org.members" v-bind:key="i" :href="(m.github.length > 5) ? m.github : '#about'">
                <div class="text-center outline-2 outline-dashed outline-[#292929] rounded-lg p-2 hover:opacity-70 transition-opacity duration-300">
                  <img :src="m.icon " class="rounded-full w-12 h-12 object-cover inline-block"/>
                  <span class="text-lg block mt-1">{{ m.name }}</span>
                  <span class="text-sm bg-[#292929] px-2 py-0.5 rounded-full block mt-1">{{ m.role }}</span>
                </div>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div id="statistics" class="bg-[#292929]">
      <div class="container mx-auto p-8 md:pb-20">
        <h1 class="text-4xl text-white text-center md:text-right">Statistics</h1>

        <section class="mb-32 text-center p-4 mt-14">

          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-x-6 items-center">

            <div class="bg-[#1d1d1d] rounded-lg mt-2 md:mt-0 p-4 md:p-0" v-for="stat in org.stats" v-bind:key="stat.num">
              
              <h5 class="text-xl md:mb-4">{{ stat.num }}<span class="text-accent">+</span></h5>
              <h6 class="text-lg">{{ stat.title }}</h6>
              
            </div>

          </div>
        </section>
      </div>
    </div>

    <div id="contact" class="">
      <div class="container mx-auto p-8 md:pb-20">
        <h1 class="text-4xl text-white text-center md:text-left">Contact</h1>

        <div class="grid md:grid-cols-2 py-4 mt-6 pb-20">
          <div>
            <h1 class="text-lg">Get in touch with us</h1>
            
            <ul>
              <li class="py-2">
                <a href="mailto:contact@projectdema.com" class="font-semibold">
                  <i class="fa-solid fa-envelope opacity-50"></i> <span class="px-2 text-accent">contact@projectdema.com</span>
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
                <a href="https://github.com/projectdema" class="font-semibold" target="_blank" rel="noopener noreferrer">
                  <i class="fa-brands fa-github opacity-50"></i> <span class="px-2 text-accent">Github</span>
                </a>
              </li>

              <li class="py-2">
                <a href="https://instagram.com/projectdema" class="font-semibold" target="_blank" rel="noopener noreferrer">
                  <i class="fa-brands fa-instagram opacity-50"></i> <span class="px-2 text-accent">Instagram</span>
                </a>
              </li>

              <li class="py-2">
                <a href="https://twitter.com/projectdema" class="font-semibold" target="_blank" rel="noopener noreferrer">
                  <i class="fa-brands fa-twitter opacity-50"></i> <span class="px-2 text-accent">Twitter</span>
                </a>
              </li>
            </ul>
            
          </div>
        </div>
      </div>
    </div>

  </main>

  <footer>
    <Footer/>
  </footer>
</template>