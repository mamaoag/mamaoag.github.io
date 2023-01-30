<template>
  <div class="block p-4 lg:flex justify-center items-center space-x-4">
    <PortfolioBlock />
  </div>
</template>

<script>
import PortfolioBlock from '../components/Home/PortfolioBlock'

export default {
  name: 'IndexPage',
  components: {
    PortfolioBlock,
  },
  head: {
    title: 'Works of Japhet Mamaoag',
  },
}
</script>
