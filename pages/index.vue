<template>
  <div class="block p-4 lg:flex justify-center items-center space-x-4">
    <IntroBlock />
    <PortfolioBlock />
  </div>
</template>

<script>
import IntroBlock from '../components/Home/IntroBlock'
import PortfolioBlock from '../components/Home/PortfolioBlock'

export default {
  name: 'IndexPage',
  components: {
    IntroBlock,
    PortfolioBlock,
  },
  head: {
    title: 'Japhet Mamaoag',
  },
}
</script>
