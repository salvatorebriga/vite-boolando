<script>
  import AppHeader from "./components/header/AppHeader.vue";
  import AppContent from "./components/content/AppContent.vue";
  import AppFooter from "./components/footer/AppFooter.vue";
  export default {
    name: "MyApp",
    data() {
      return {};
    },
    components: {
      AppHeader,
      AppContent,
      AppFooter,
    },
  };
</script>

<template>
  <AppHeader />
  <AppContent />
  <AppFooter />
</template>
