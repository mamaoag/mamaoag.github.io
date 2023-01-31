<template>
  <div class="relative border-2 border-black p-4 group h-48 w-48 group hover:cursor-pointer mt-2 ease-in">
      <img :src="experience.image" class="relative h-full w-full grayscale group-hover:0 group-hover:grayscale-0" :alt="experience.company">
      <div class="absolute inset-x-0 bottom-0 hidden text-center group-hover:block w-full p-2">
        <h1 class="text-xs tracking-[3.5%] font-bold">{{ experience.title }} ({{experience.active}})</h1>
      </div>
  </div>
</template>

<script>
export default {
  name: 'AboutExperience',
  props: {
    experience: Object,
  },
}
</script>
