<script>
import FooterTop from './FooterTop.vue';

export default {
  components: { FooterTop },
  data() {

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
  height: calc(100vh - 530px);
  background-image: url('../assets/img/dc-logo-bg.png'), url('../assets/img/footer-bg.jpg');
  background-repeat: no-repeat, no-repeat;
  background-size: 600px, cover;
  background-position: center;
  background-position-x: 1000px, 0;
}
</style>