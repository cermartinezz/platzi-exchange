<template>
  <button
    @click="coinDetails"
    class="bg-tramsparent hover:bg-green-500 text-green-700 font-semibold"
  >
    <beat-loader
      :loading="isLoading"
      :color="'#68d391'"
      :size="8"
    ></beat-loader>
    <slot v-show="isLoading"></slot>
  </button>
</template>

<script>
export default {
  name: "PxButtom",
  props: { isLoading: { type: Boolean, default: false } },
  methods: {
    coinDetails() {
      this.$emit("on-touch");
    }
  }
};
</script>
