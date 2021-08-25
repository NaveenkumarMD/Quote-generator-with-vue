<template>
  <Topbar />
  <Quote />
</template>

<script>
import QuoteVue from "./components/Quote.vue";
import TopbarVue from "./components/Topbar.vue";

export default {
  name: "App",
  components: {
    Topbar: TopbarVue,
    Quote: QuoteVue,
  },
};
</script>

<style>
#app {
  padding: 0;
  margin: 0;
}
</style>
