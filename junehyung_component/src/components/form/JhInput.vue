<template>
  <div class="input-wrap-box row items-center">
    <div v-if="preffix" class="preffix-box">
      <span>{{ preffix }}</span>
    </div>
    <input
      type="text"
      v-model="getData"
      :disabled="disabled"
      :maxlength="maxLength"
      :placeholder="placeholder"
    />
    <div v-if="suffix" class="suffix-box">
      <span>{{ suffix }}</span>
    </div>
    <div v-if="allowClear" @click="clearValue">X</div>
  </div>
</template>

<script setup>
import { ref, defineProps } from "vue";

const props = defineProps([
  "value",
  "disabled",
  "maxLength",
  "placeholder",
  "preffix",
  "suffix",
  "allowClear",
]);
const getData = ref(props.value);
const clearValue = () => {
  console.log(getData.value.value);
  getData.value.value = null;
};
</script>
