<template>
  <div>
    <slot />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "Box",
  data: () => ({}),
});
</script>
