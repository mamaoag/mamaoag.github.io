<template>
  <div class="block p-4 mt-12">
    <ImageBlock :project="showcase" />
    <div class="block lg:flex justify-center items-center space-x-4">
      <PortfolioBlock :portfolio="showcase" />
      <SkillBlock :skills="showcase.skills" />
    </div>
  </div>
</template>

<script>
import ImageBlock from '../../components/Portfolio/Blocks/ImageBlock'
import PortfolioBlock from '../../components/Portfolio/PortfolioBlock'
import SkillBlock from '../../components/Portfolio/SkillBlock.vue'

export default {
  name: 'IndexPage',
  components: {
    PortfolioBlock,
    SkillBlock,
    ImageBlock,
  },
  data() {
    return {
      showcase: {},
      projects: [
        {
          id: 'the-frazzled-cook',
          title: 'The Frazzled Cook',
          img: '/portfolio/tfc.png',
          category: 'Client Project',
          url: '/portfolio/the-frazzled-cook',
          cta: 'https://www.thefrazzledcook.net',
          description:
            'is founded by LeeChoaChengCo Inc., a group of four ladies who have partnered up to bring to life this quaint little restaurant located along Scout Gandia Street in the heart of the Tomas Morato area in Quezon City.',
          skills: [
            {
              title: 'Back-end Development',
              icon: 'fa-solid fa-terminal',
              skills: [],
            },
            {
              title: 'Front-end Development',
              icon: 'fa-solid fa-laptop-code',
              skills: [],
            },
          ],
        },
        {
          id: 'binosearch',
          title: 'Binosearch',
          img: '/portfolio/bnc.png',
          category: 'Personal Project',
          url: '/portfolio/binosearch',
          cta: 'https://www.github.com/mamaoag/binosearch',
          description:
            'is an auxiliary scanner written in Go that checks if your API is vulnerable to OWASP Top 10 API vulnerabilities.',
          skills: [
            {
              title: 'CLI Development',
              icon: 'fa-solid fa-terminal',
              skills: [],
            },
          ],
        },
      ],
    }
  },
  head: {
    title: `Work of Japhet Mamaoag`,
  },
  mounted() {
    const slug = this.$route.params.slug
    const showcase = this.projects.find((p) => p.id === slug)

    if (!showcase) {
      return this.$nuxt.error({ statusCode: 404, message: 'Not Found' })
    }

    this.showcase = showcase
  },
}
</script>
