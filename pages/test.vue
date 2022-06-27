<template>
  <div>adsfasdfasdfas</div>
</template>
<script>
import axios from "axios";
import { mapMutations } from "vuex";
export default {
  computed: {
    cart() {
      return this.$store.state.cart;
    },
  },
  methods: {
    addTodo(item) {
      this.$store.commit("cart/add", item);
    },
    ...mapMutations({
      toggle: "cart/toggle",
    }),
  },
};
</script>
