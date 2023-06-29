<script>
export default {
  data() {
    return {
      lists: [
        {
          text: 'Characters',
          url: '#',
          current: false,
        },
        {
          text: 'Comics',
          url: '#',
          current: true,
        },
        {
          text: 'Movies',
          url: '#',
          current: false,
        },
        {
          text: 'TV',
          url: '#',
          current: false,
        },
        {
          text: 'Games',
          url: '#',
          current: false,
        },
        {
          text: 'Collectibles',
          url: '#',
          current: false,
        },
        {
          text: 'Videos',
          url: '#',
          current: false,
        },
        {
          text: 'Fans',
          url: '#',
          current: false,
        },
        {
          text: 'News',
          url: '#',
          current: false,
        },
        {
          text: 'Shop',
          url: '#',
          current: false,
        },
      ]

    }
  }
}
</script>

<template>
  <header class="container">
    <figure>
      <img src="../assets/img/dc-logo.png" alt="Logo">
    </figure>
    <nav>
      <ul>
        <li v-for="list in lists" :key="list.text" :class="{ active: list.current }"><a :href="list.url">{{ list.text
        }}</a></li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
@use '../assets/sass/_mixins.scss' as *;
@use '../assets/sass/_variable.scss' as *;

header {
  height: 100px;
  @include flex-center-y;
  justify-content: space-between;

}

/* LOGO */
img {
  max-width: 100%;
  width: 70px;
}

/* NAV BAR */
nav {
  height: 100%;
}

ul {
  @include flex-center;
  gap: 25px;
  height: 100%;

  li {
    @include flex-center-y;
    height: 100%;

    &.active {
      box-shadow: 0 5px $blue;
      color: $blue;
    }
  }
}
</style>