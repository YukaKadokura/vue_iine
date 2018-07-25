<template>
  <div>
    <div>TOTAL: {{ total }}</div>
		<like-component message="AAA" v-on:increment="incrementTotal"></like-component>
		<like-component message="BBB" v-on:increment="incrementTotal"></like-component>
		<like-component message="CCC" v-on:increment="incrementTotal"></like-component>
		<like-component v-on:increment="incrementTotal"></like-component>
  </div>
</template>

<script>
import likeComponent from "./components/likeComponent.vue";

export default {
  name: "app",
  data: function() {
    return {
      total: 0
    };
  },
  methods: {
    incrementTotal: function() {
      this.total++;
    }
  },
  components: {
    likeComponent
  }
};
</script>
