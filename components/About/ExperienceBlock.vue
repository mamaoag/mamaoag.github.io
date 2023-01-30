<template>
  <div class="w-full mt-8">
    <h3 class="text-lg tracking-[3.5%] underline">My Experience</h3>
    <Showcase
      v-for="project in showcase"
      :key="project.title"
      :project="project"
    />
  </div>
</template>

<script>
import Showcase from '../Home/Portfolio/Showcase'

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
