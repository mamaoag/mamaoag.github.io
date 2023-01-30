<template>
  <div>
    <!-- Header -->
    <div class="flex justify-start space-x-4 mt-4 items-center">
      <div class="group relative inline-block focus:ring-0">
        <span
          class="absolute inset-0 translate-x-1.5 translate-y-1.5 bg-yellow-300 transition-transform group-hover:translate-y-0 group-hover:translate-x-0 ease-in"
        ></span>
        <span
          class="relative px-2 py-1 border-2 border-black inline-block text-lg"
        >
          <i :class="`${skill.icon} text-sm`"></i>
        </span>
      </div>
      <h4 class="text-base tracking-[3.5%] leading-[32px]">
        {{ skill.title }}
      </h4>
    </div>
    <div
      v-if="skill & skill.skills"
      class="mt-4"
      v-html="singleText(skill.skills)"
    ></div>
    <!-- Content -->
  </div>
</template>

<script>
export default {
  name: 'AboutSkill',
  props: {
    skill: Object,
  },
  methods: {
    singleText(skills) {
      let text = ''

      skills.forEach((s, i) => {
        text +=
          i !== skills.length - 1
            ? `<span class="font-bold">${s.main}</span>${
                s.sub ? ` ${s.sub}` : ''
              }, `
            : `<span class="font-bold">${s.main}</span>${s.sub}`
      })

      return text
    },
  },
}
</script>
