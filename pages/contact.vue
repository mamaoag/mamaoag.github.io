<template>
  <div class="block p-4 lg:flex justify-center items-center space-x-4">
    <ContactBlock />
  </div>
</template>

<script>
import ContactBlock from '../components/Contact/ContactBlock'
export default {
  name: 'ContactPage',
  components: {
    ContactBlock,
  },
}
</script>
