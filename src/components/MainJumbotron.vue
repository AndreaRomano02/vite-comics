<script>
import JumbotronBgImage from './MainBgImage.vue';

export default {
  components: { JumbotronBgImage },
  props: {
    games: Array,
  },
  data() {
    return {
    }
  }
}
</script>

<template>
  <div id="jumbotron">
    <JumbotronBgImage />

    <div class="container card-container">

      <!-- Ho dovuto mettere la mustrush sintax poichè mi dava errore se lo scrivevo normalmente  -->
      <a href="#">
        <h2> {{ '--> Content goes here < --' }} </h2>
      </a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/sass/_mixins.scss' as *;
@use '../assets/sass/_variable.scss' as *;

#jumbotron {
  background-color: $bg_jumbo;
  color: white;
  font-weight: 900;
}

.card-container {
  height: 100%;
  @include flex-center-y
}
</style>