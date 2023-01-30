<template>
  <div class="block p-4 lg:flex justify-center items-center space-x-4">
    <div class="mx-8 mt-8">
      <div class="intro-heading-block lg:w-full">
        <img src="/404.svg" alt="404 image" class="w-[300px]" />
        <h2 class="text-2xl mt-4">Oops!</h2>
        <h1 class="text-4xl">
          <span class="group relative inline-block">
            <span
              class="absolute inset-x-0 translate-y-6 bg-yellow-300 transition-transform group-hover:translate-y-0 group-hover:translate-x-0 h-1/2 group-hover:h-full group-hover:cursor-pointer"
            ></span>
            <span class="font-bold underline relative inline-block"
              >Wrong Page</span
            >
          </span>
        </h1>
      </div>
      <div class="intro-content-block">
        <p class="text-base w-full mt-4 leading-[32px]">
          Looks like you are
          <span class="font-bold tracking-widest">LOST!</span>
        </p>
        <NuxtLink to="/" class="group relative inline-block focus:ring-0 mt-4">
          <span
            class="absolute inset-0 translate-x-1.5 translate-y-1.5 bg-yellow-300 transition-transform group-hover:translate-y-0 group-hover:translate-x-0 ease-in"
          ></span>
          <span
            class="relative inline-block px-8 py-3 text-base tracking-wide border-2 border-black"
            >Go back Home</span
          >
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'error',
  props: ['errors'],
}
</script>
