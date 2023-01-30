<template>
  <div class="block p-4 lg:flex justify-center items-center space-x-4">
    <AboutBlock />
    <div class="mx-8 mt-8 w-full">
      <SkillBlock />
      <ExperienceBlock />
    </div>
  </div>
</template>

<script>
import AboutBlock from '../components/About/AboutBlock'
import SkillBlock from '../components/About/SkillBlock'
import ExperienceBlock from '../components/About/ExperienceBlock'

export default {
  name: 'AboutPage',
  components: {
    AboutBlock,
    SkillBlock,
    ExperienceBlock,
  },
  head: {
    title: 'Who is Japhet Mamaoag',
  },
}
</script>
