<template>
  <h3>{{ title }}</h3>
</template>
<script>
import Vue from "vue";
export default Vue.extend({
  props: ["title"],
});
</script>
<style scoped>
h3 {
  width: 100%;
  font-weight: normal;
}
</style>
