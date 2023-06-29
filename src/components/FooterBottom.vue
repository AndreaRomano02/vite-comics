<script>
export default {
  data() {
    return {
      footerImages: [
        {
          image: 'footer-facebook.png',
          text: 'Facebook'
        },
        {
          image: 'footer-twitter.png',
          text: 'Twitter'
        },
        {
          image: 'footer-youtube.png',
          text: 'YouTube'
        },
        {
          image: 'footer-pinterest.png',
          text: 'Pinterest'
        },
        {
          image: 'footer-periscope.png',
          text: 'Periscope'
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
  <div class="bg-bottom-foot">
    <div class="footer-bottom container">
      <div class="left">
        <button>SING-UP NOW!</button>
      </div>
      <div class="right">
        <a href="#">
          <h3>FOLLOW US</h3>
        </a>
        <figure>
          <a v-for="footerImage in footerImages" :href="footerImage.text">
            <img :src="getImagePath(footerImage.image)" :alt="footerImage.text">
          </a>
        </figure>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../assets/sass/_variable.scss' as *;
@use '../assets/sass/_mixins.scss' as *;

.bg-bottom-foot {
  background-color: $bg_footer;
}

.footer-bottom {
  height: 100px;

  @include flex-center-y;

  justify-content: space-between;

  .left {

    button {
      color: white;
      font-size: 1.2rem;
      padding: 15px;
      border: 2px solid $blue;
      background-color: transparent;
      cursor: pointer;
      transition: background-color 0.5s;

      &:hover {
        background-color: gray;
      }
    }
  }

  .right {
    display: flex;

    h3 {
      color: $blue;
      font-weight: bolder;
    }

    img {
      margin-left: 20px;
    }
  }
}
</style>