<template>
  <div>
    <span v-for="r in repetitions" :key="r">
      {{ content }}
    </span>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "Repeat",
  props: {
    times: {
      type: Number,
    },
    config: {
      type: Object,
      validator(value) {
        return (
          typeof value.times === "number" && typeof value.content === "string"
        );
      },
    },
    content: {
      type: [String, Number],
    },
    todoListPromise: {
      type: Promise,
    },
  },
  computed: {
    repetitions() {
      return Array.from({ length: this.times });
    },
  },
});
</script>

