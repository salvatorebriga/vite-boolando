<script>
  import AppHeader from "./components/header/AppHeader.vue";
  import AppContent from "./components/content/AppContent.vue";
  export default {
    name: "MyApp",
    data() {
      return {};
    },
    components: {
      AppHeader,
      AppContent,
    },
  };
</script>

<template>
  <AppHeader />
  <AppContent />
</template>
