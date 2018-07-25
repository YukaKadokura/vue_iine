<template>
  <button @click="countUp">{{ message }} {{ count }}</button>
</template>

<script>
export default {
  name: "like-component",
  data: function() {
    return {
      count: 0
    };
  },
  props: {
    message: {
      type: String,
      default: "ZZZ"
    }
  },
  methods: {
    countUp: function() {
      this.count++;
      this.$emit("increment");
    }
  }
};
</script>
