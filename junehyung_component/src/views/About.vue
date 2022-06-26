<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
  <div>
    <JhInput
      :value="nameInput"
      preffix="1"
      suffix=" 입니다."
      placeholder="이름입력하세요."
      :allowClear="true"
      :maxLength="10"
      :disabled="inputDisabled"
      style="width: 260px"
      @input="handleInput"
    ></JhInput>
    <CommonInput v-model:value="nameInput"></CommonInput>
  </div>
  <div class="result-box">
    <p>input : {{ nameInput }}</p>
  </div>
  <button @click="test">TEST</button>
</template>
<script setup>
import { ref } from "vue";
import JhInput from "@/components/form/JhInput.vue";
import CommonInput from "@/components/form/CommonInput.vue";
const nameInput = ref(null);
const inputDisabled = ref(false);
const test = () => {
  inputDisabled.value = !inputDisabled.value;
  console.log(nameInput.value);
};

const handleInput = (value) => {
  nameInput.value = value;
};
</script>

<style lang="scss" scoped>
.result-box {
  height: 50%;
  border: 1px solid #d9d9d9;
}
</style>
