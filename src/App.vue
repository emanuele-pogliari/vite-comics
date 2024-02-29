<script>
import AppNav from './components/AppNav.vue';
import AppContent from './components/AppContent.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppNav,
    AppContent,
    AppFooter,
  }
}

</script>

<template>
  <AppNav></AppNav>
  <AppContent></AppContent>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@use './styles/general' as *;
@use './styles/variables' as *;
@use './styles/mixins' as *;
</style>
