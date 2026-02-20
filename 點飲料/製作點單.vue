<script setup>
import { ref } from "vue";
const drink = ref("");
const sweetness = ref("");
const ice = ref("");
</script>

<template>
  <h3>飲料點單</h3>

  <!-- 步驟 1 -->
  <fieldset>
    <legend>步驟 1：選擇飲料</legend>

    <label>
      紅茶
      <input v-model="drink" type="radio" name="drink" value="紅茶"
    /></label>

    <label>
      綠茶
      <input v-model="drink" type="radio" name="drink" value="綠茶"
    /></label>
  </fieldset>

  <!-- 步驟 2 -->
  <fieldset v-if="drink">
    <legend>步驟 2：甜度</legend>
    <label>
      正常甜
      <input v-model="sweetness" type="radio" name="sweetness" value="正常甜"
    /></label>

    <label>
      無糖
      <input v-model="sweetness" type="radio" name="sweetness" value="無糖"
    /></label>
  </fieldset>

  <!-- 步驟 3 -->
  <fieldset v-if="sweetness">
    <legend>步驟 3：冰量</legend>
    <label>
      正常冰
      <input v-model="ice" type="radio" name="ice" value="正常冰"
    /></label>

    <label>
      去冰
      <input v-model="ice" type="radio" name="ice" value="去冰"
    /></label>
  </fieldset>
</template>
