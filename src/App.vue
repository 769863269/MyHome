<script setup>
import pageLoad from "./components/page-load.vue";
import home from "./components/home.vue";
import { onMounted, ref } from "vue";

const isLoad = ref(true);
onMounted(() => {
  setTimeout(() => {
    isLoad.value = false;
  }, 2000);
});
</script>

<template>
  <pageLoad v-if="isLoad"></pageLoad>
  <div class="wrapper" v-else>
    <home></home>
  </div>
</template>

<style lang="scss" scoped></style>
