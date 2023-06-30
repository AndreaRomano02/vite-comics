<script>
import MainJumbotron from './MainJumbotron.vue';

export default {
  components: { MainJumbotron },
  props: {
    comics: Array,
  },
  data() {
    return {
      mainLists: [
        {
          image: 'buy-comics-digital-comics.png',
          text: 'Digital Comics'
        },
        {
          image: 'buy-comics-merchandise.png',
          text: 'Dc Merchandise'
        },
        {
          image: 'buy-comics-subscriptions.png',
          text: 'Subscription'
        },
        {
          image: 'buy-comics-shop-locator.png',
          text: 'Comic Shop Locator'
        },
        {
          image: 'buy-dc-power-visa.svg',
          text: 'Dc Power Visa'
        },
      ]
    }
  },
  methods: {
    getImagePath(image) {
      return new URL(`../assets/img/${image}`, import.meta.url).href;
    }
  }
}
</script>

<template>
  <main>
    <MainJumbotron :comics="comics" />

    <section>
      <nav class="container">
        <ul>
          <li v-for="mainList in mainLists">
            <a href="#">
              <img :src="getImagePath(mainList.image)" :alt="mainList.text">
              <p>{{ mainList.text }}</p>
            </a>
          </li>
        </ul>
      </nav>
    </section>
  </main>
</template>

<style lang="scss" scoped>
@use '../assets/sass/_mixins.scss' as *;
@use '../assets/sass/_variable.scss' as *;

section {
  background-color: $blue;
  height: 150px;
  color: white;
}

nav {
  height: 100%;
}

ul {
  height: 100%;
  @include flex-center-y;
  justify-content: space-between;

  a {
    @include flex-center-y;

    img {
      max-width: 100%;
      height: 60px;
    }

    p {
      margin-left: 10px;
    }
  }




}
</style>