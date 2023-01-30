<template>
  <div class="mx-8 mt-8 w-full">
    <h3 class="text-lg tracking-[3.5%] underline">Featured Works</h3>
    <Showcase
      v-for="project in showcase"
      :key="project.title"
      :project="project"
    />
  </div>
</template>

<script>
import Showcase from './Portfolio/Showcase'

export default {
  components: {
    Showcase,
  },
  data() {
    return {
      showcase: [
        {
          title: 'The Frazzled Cook',
          img: '/portfolio/tfc.png',
          category: 'Client Project / e-Commerce',
          url: '/portfolio/the-frazzled-cook',
        },
        {
          title: 'Binosearch',
          img: '/portfolio/bnc.png',
          category: 'Personal Project / Security Tool',
          url: '/portfolio/binosearch',
        },
      ],
    }
  },
}
</script>
