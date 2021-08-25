<template>
  <div id="bar">
    <div id="title">Quotes generator</div>
  </div>
</template>
<script>
export default {
  name: "Topbar",
};
</script>
<style scoped>
#bar {
  background-color: rgb(1, 167, 42);
  margin: 0;
  height: 50px;
  color: white;
  display: flex;
  align-items: center;
}
#title {
  font-size: 22px;
  padding-left: 20px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
</style>