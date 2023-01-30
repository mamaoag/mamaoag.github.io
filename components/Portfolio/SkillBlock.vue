<template>
  <div class="w-full">
    <h3 class="text-lg tracking-[3.5%] underline">Role</h3>
    <Skill v-for="skill in skills" :key="skill.title" :skill="skill" />
  </div>
</template>

<script>
import Skill from '../About/Blocks/Skill.vue'

export default {
  components: {
    Skill,
  },
  props: {
    skills: Object,
  },
}
</script>
