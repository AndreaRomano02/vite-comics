<script>
import JumbotronBgImage from './MainBgImage.vue';

export default {
  components: { JumbotronBgImage },
  props: {
    comics: Array,
  },
  data() {
    return {
      load: false,
      messageButton: 'LOAD MORE',
    }
  },
  methods: {
    isLoaded() {
      this.load = !this.load;
      if (this.messageButton === 'LOAD MORE') this.messageButton = 'LOAD LESS'
      else this.messageButton = 'LOAD MORE'
    },
  },
}
</script>

<template>
  <div id="jumbotron">
    <JumbotronBgImage />
    <div class="container card-container">
      <div class="current">CURRENT SERIES</div>
      <div v-for="game in comics" class="card">
        <figure>
          <img :src="game.thumb" :alt="game.series">
          <figcaption>{{ game.series }}</figcaption>
        </figure>
      </div>

      <div v-for="game in comics" class="card" v-show="load">
        <figure>
          <img :src="game.thumb" :alt="game.series">
          <figcaption>{{ game.series }}</figcaption>
        </figure>
      </div>

      <button @click="isLoaded">{{ messageButton }}</button>

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
  padding: 3rem 0;
  @include flex-center;
  flex-wrap: wrap;

  position: relative;
}

.card {
  width: calc(100% / 6);
  height: 300px;

  padding: 0 1rem;
  font-size: 0.9rem;
}

img {
  display: block;
  max-width: 100%;
  height: 200px;
  width: 200px;
  object-fit: cover;

  margin-bottom: 20px;
}

.current {
  background-color: $blue;
  display: inline-block;
  padding: 1rem 2rem;
  font-size: 1.3rem;
  font-weight: bolder;

  position: absolute;
  left: 15px;
  top: -35px;
}

button {
  background-color: $blue;
  border: none;
  color: white;
  font-weight: bolder;
  padding: 0.8rem 3rem;
  cursor: pointer;

}
</style>