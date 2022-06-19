<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
  <div class="box-wrap">
    <div class="testBox bg-red-13 jh-mx-sm"></div>
    <div class="testBox bg-pink-13 jh-mx-sm"></div>
    <div class="testBox bg-purple-13 jh-mx-sm"></div>
    <div class="testBox bg-deep-purple-13 jh-mx-sm"></div>
    <div class="testBox bg-indigo-13 jh-mx-sm"></div>
    <div class="testBox bg-blue-13 jh-mx-sm"></div>
    <div class="testBox bg-light-blue-13 jh-mx-sm"></div>
    <div class="testBox bg-cyan-13 jh-mx-sm"></div>
    <div class="testBox bg-teal-13 jh-mx-sm"></div>
    <div class="testBox bg-green-13 jh-mx-sm"></div>

    <div class="testBox bg-light-green-13 jh-mx-sm"></div>
    <div class="testBox bg-lime-13 jh-mx-sm"></div>
    <div class="testBox bg-yellow-13 jh-mx-sm"></div>
    <div class="testBox bg-amber-13 jh-mx-sm"></div>
    <div class="testBox bg-orange-13 jh-mx-sm"></div>
    <div class="testBox bg-deep-orange-13 jh-mx-sm"></div>
    <div class="testBox bg-brown-4 jh-mx-sm"></div>
    <div class="testBox bg-grey-4 jh-mx-sm"></div>
    <div class="testBox bg-blue-grey-4 jh-mx-sm"></div>
  </div>
  <div class="testBox bg-red-5 jh-my-sm"></div>
  <div class="testBox bg-purple-5"></div>
</template>
<style lang="scss" scoped>
.box-wrap {
  display: flex;
  flex-direction: row;
}
.testBox {
  width: 200px;
  height: 200px;
  border: 1px solid #ddd;
  flex: 1;
}
.testBox2 {
  width: 200px;
  height: 200px;
  background-color: $bgColor2;
}
</style>
