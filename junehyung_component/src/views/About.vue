<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
  <div>
    <JhInput
      :value="nameInput"
      preffix="글자 : "
      suffix=" 입니다."
      placeholder="이름입력하세요."
      :allowClear="true"
      :maxLength="10"
      :disabled="inputDisabled"
      style="width: 260px"
      @input="handleInput"
    ></JhInput>
    <JhInputNumber
      :value="inputNumber"
      preffix="숫자 : "
      suffix=" 입니다."
      placeholder="숫자입력하세요."
      :allowClear="true"
      :disabled="inputDisabled"
      style="width: 260px"
      @input="handleInputNumber"
    ></JhInputNumber>
  </div>
  <div class="result-box">
    <p>input : {{ nameInput }}</p>
    <p>number : {{ inputNumber }}</p>
  </div>
  <button @click="test">TEST</button>
</template>
<script setup>
import { ref } from "vue";
import JhInput from "@/components/form/JhInput.vue";
import JhInputNumber from "@/components/form/JhInput.vue";
// import CommonInput from "@/components/form/CommonInput.vue";
const nameInput = ref(null);
const inputNumber = ref(null);

const inputDisabled = ref(false);
const test = () => {
  inputDisabled.value = !inputDisabled.value;
  console.log(nameInput.value);
};

const handleInput = (value) => {
  nameInput.value = value;
};
const handleInputNumber = (value) => {
  inputNumber.value = value;
};
</script>

<style lang="scss" scoped>
.result-box {
  height: 50%;
  border: 1px solid #d9d9d9;
}
</style>
