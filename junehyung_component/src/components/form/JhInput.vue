<template>
  <div class="input-wrap-box">
    <div v-if="preffix">
      <span>{{ preffix }}</span>
    </div>
    <input
      type="text"
      :value="value"
      :disabled="disabled"
      :maxlength="maxLength"
      :placeholder="placeholder"
    />
    <div v-if="suffix">
      <span>{{ suffix }}</span>
    </div>
    <div v-if="allowClear">X</div>
  </div>
</template>

<script setup lang="ts">
import { ref, defineProps } from "vue";

interface Props {
  value: string;
  preffix: string;
  suffix: string;
  placeholder: string;
  maxLength: number;
  disabled: boolean;
  allowClear: boolean;
}
const props = defineProps<Props>();
</script>
