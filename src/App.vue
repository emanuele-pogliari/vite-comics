<script>
import AppNav from './components/AppNav.vue';
import AppContent from './components/AppContent.vue';
import AppEcommerce from './components/AppEcommerce.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppNav,
    AppContent,
    AppEcommerce,
    AppFooter,
  }
}

</script>

<template>
  <AppNav></AppNav>
  <AppContent></AppContent>
  <AppEcommerce></AppEcommerce>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@use './styles/general' as *;
</style>
