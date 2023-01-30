<template>
  <a :href="project.url" class="group relative">
    <div class="p-2 block lg:flex mt-4 lg:h-[254px]">
      <div
        class="border-2 border-black p-2 lg:rotate-180 lg:[writing-mode:_vertical-lr] group-hover:hidden"
      >
        <span class="text-sm">{{ project.category }}</span>
        <h5 class="text-sm font-bold tracking-[5%]">
          {{ project.title }}
        </h5>
      </div>
      <div class="w-full lg:w-[549px]">
        <img
          :src="project.img"
          alt=""
          class="w-full h-full border-2 border-black object-cover object-center lg:border-l-0 group-hover:border-l-2 group-hover:scale-105"
        />
      </div>
    </div>
  </a>
</template>

<script>
export default {
  name: 'PortfolioShowcase',
  props: {
    project: Object,
  },
}
</script>
