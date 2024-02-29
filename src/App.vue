<script>
import AppNav from './components/AppNav.vue';
import AppContent from './components/AppContent.vue';

export default {
  components: {
    AppNav,
    AppContent,
  }
}

</script>

<template>
  <AppNav>ciao</AppNav>
  <AppContent></AppContent>
</template>

<style lang="scss">
@use './styles/general' as *;
</style>
