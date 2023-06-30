<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import comics from './assets/data/_comics.js'
export default {
  components: { AppHeader, AppMain, AppFooter },
  data() {
    return {
      comics
    }
  }
};
</script>

<template>
  <AppHeader />

  <AppMain :comics="comics" />

  <AppFooter />
</template>

<style lang="scss">
@use './assets/sass/style.scss' as *;
</style>
