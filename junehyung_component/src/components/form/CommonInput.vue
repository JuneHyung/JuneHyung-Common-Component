<template>
  <JhInput :value="getValue.value" @input="handleInput"></JhInput>
</template>
<script setup>
import { ref, defineProps } from "vue";
import JhInput from "./JhInput.vue";
const props = defineProps([
  "value",
  "disabled",
  "maxLength",
  "placeholder",
  "preffix",
  "suffix",
  "allowClear",
]);
const getValue = ref(props);
const handleInput = (value) => {
  getValue.value.value = value;
};
</script>
<style lang="sass" scoped></style>
