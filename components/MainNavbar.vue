<template>
  <nav class="p-4 w-full">
    <NuxtLink to="/">
      <div id="nav-logo">
        <h1 class="font-bold text-2xl">KYJPT</h1>
      </div>
    </NuxtLink>
    <ul class="block mt-2">
      <li v-for="(link, idx) in navLinks" :key="idx">
        <a class="group relative inline-block" :href="link.route">
          <span
            :class="{ 'bg-yellow-300': $route.path == link.route }"
            class="absolute inset-0 translate-y-6 group-hover:bg-yellow-300 transition-transform h-1/4 ease-in"
          ></span>
          <span
            :class="{ underline: $route.path == link.route }"
            class="group-hover:underline uppercase relative font-bold tracking-widest inline-block px-2 py-3"
            >{{ link.name }}</span
          >
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      navLinks: [
        { route: '/about', name: 'About' },
        { route: '/works', name: 'Works' },
        { route: '/contact', name: 'Message' },
      ],
    }
  },
}
</script>
