<template>
  <div class="w-full">
    <h3 class="text-lg tracking-[3.5%] underline">My Skills</h3>
    <Skill v-for="skill in skills" :key="skill.title" :skill="skill" />
  </div>
</template>

<script>
import Skill from './Blocks/Skill.vue'

export default {
  components: {
    Skill,
  },
  data() {
    return {
      skills: [
        {
          title: 'Back-end Development',
          icon: 'fa-solid fa-terminal',
          skills: [
            { main: 'PHP', sub: '(Laravel / CodeIgniter / Symfony)' },
            { main: 'Ruby', sub: '(Ruby on Rails)' },
            { main: 'NodeJS', sub: '(Express)' },
          ],
        },
        {
          title: 'Front-end Development',
          icon: 'fa-solid fa-laptop-code',
          skills: [
            { main: 'HTML', sub: '' },
            { main: 'CSS', sub: '(TailwindCSS / Bootstrap / MUI / Bulma)' },
            { main: 'JavaScript', sub: '(Vue / React)' },
            { main: 'TypeScript', sub: '' },
          ],
        },
        {
          title: 'Others',
          icon: 'fa-solid fa-earth-asia',
          skills: [
            { main: 'Linux', sub: '' },
            { main: 'Cloud Platform', sub: '(AWS / DigitalOcean / GCP)' },
            { main: 'Docker', sub: '' },
            { main: 'Version Control', sub: '(Git)' },
          ],
        },
      ],
    }
  },
}
</script>
