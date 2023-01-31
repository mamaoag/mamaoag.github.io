<template>
  <div class="w-full mt-8">
    <h3 class="text-lg tracking-[3.5%] underline">My Experience</h3>
    <div class="flex justify-start items-center space-x-4">
      <Experience
        v-for="experience in showcase"
        :key="experience.title"
        :experience="experience"
      />
    </div>
  </div>
</template>

<script>
import Experience from './Blocks/Experience';

export default {
  components: {
    Experience
  },
  data() {
    return {
      showcase: [
        {
          title: 'IT Specialist',
          image: '/experience/zpc.png',
          active: '2022 - Current',
          company: 'Zuellig Pharma',
        },
        {
          title: 'Software Engineer',
          image: '/experience/crh.jpg',
          active: '2020 - 2022',
          company: 'CREATIVEHOPE PH INC.',
        },
        {
          title: 'Instructor I',
          image: '/experience/feutech.png',
          active: '2018 - 2022',
          company: 'FEU Institute of Technology',
        },
      ],
    }
  },
}
</script>
