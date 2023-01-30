<template>
  <div class="group relative p-2 block lg:flex mt-12 lg:h-[300px]">
    <div
      class="border-2 border-black p-2 lg:rotate-180 lg:[writing-mode:_vertical-lr]"
    >
      <h5 class="text-sm font-bold tracking-[5%] text-center">
        {{ project.title }}
      </h5>
    </div>
    <div class="w-full lg:w-[90vw]">
      <img
        :src="project.img"
        alt=""
        class="w-full h-full border-2 border-black object-cover object-center lg:border-l-0 group-hover:border-l-2"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'PortfolioShowcase',
  props: {
    project: Object,
  },
}
</script>
