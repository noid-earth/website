<template>
    <nav class="mt-2 py-4 rounded-lg">
      <div class="flex flex-wrap items-center justify-between">

        <a href="/">
          <span class="text-xl font-semibold ml-4">Noid<span class="text-accent">Earth</span></span>
        </a>
      </div>
    </nav>
</template>

<script lang="ts">
export default {
  name: 'Header',
  mounted() {
    if (location.protocol !== 'https:' && location.hostname === 'noid.earth') {
      location.replace(`https:${location.href.substring(location.protocol.length)}`);
    }
  }
}
</script>