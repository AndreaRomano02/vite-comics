<script>
import FooterTop from './FooterTop.vue';
import FooterBottom from './FooterBottom.vue';

export default {
  components: { FooterTop, FooterBottom },
  data() {
    return {
    }

  }
}
</script>

<template>
  <footer>
    <FooterTop />

  </footer>
</template>

<style scoped>
footer {
  color: white;
}
</style>