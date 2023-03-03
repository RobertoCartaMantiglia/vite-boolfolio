<script>
import AppMain from './components/AppMain.vue';
import AppHeader from './components/AppHeader.vue';


export default {
  name: 'App',
  components: {
    AppMain,
    AppHeader

  },

}
</script>

<template>
  <header>
    <AppHeader />
    <router-view></router-view>
  </header>

  <main>
    <!-- <AppMain /> -->


  </main>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use 'bootstrap/scss/bootstrap' as *;

.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
