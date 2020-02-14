<template>
  <button
    @click="coinDetails"
    class="bg-tramsparent hover:bg-green-500 text-green-700 font-semibold"
  >
    <slot></slot>
  </button>
</template>


<script>
export default {
  name: "PxButtom",

  methods: {
    coinDetails() {
      this.$emit("on-touch");
    }
  }
};
</script>