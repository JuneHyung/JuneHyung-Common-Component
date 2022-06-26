<template>
  <div class="input-wrap-box row items-center">
    <div v-if="preffix" class="preffix-box">
      <span>{{ preffix }}</span>
    </div>
    <input
      type="number"
      :value="value"
      :disabled="disabled"
      :maxlength="maxLength"
      :placeholder="placeholder"
      step
      @input="handleInput"
    />
    <div v-if="suffix" class="suffix-box">
      <span>{{ suffix }}</span>
    </div>
    <div v-if="allowClear" @click="clearValue">X</div>
  </div>
</template>

<script setup>
/**
 * allowClear
 * disabled
 * formatter
 * parser
 * max
 * min
 * prefix
 * suffix
 * step
 * value
 *
 */
import { ref, defineProps, defineEmits, computed } from "vue";

const props = defineProps([
  "value",
  "disabled",
  "maxLength",
  "placeholder",
  "preffix",
  "suffix",
  "allowClear",
]);
const emits = defineEmits(["input"]);

const handleInput = (event) => {
  console.log(event);
  emits("input", event.target.value);
};

const getData = ref(props.value);
const clearValue = () => {
  console.log(getData.value.value);
  getData.value.value = null;
};
</script>
