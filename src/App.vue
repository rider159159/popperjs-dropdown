<template>
  <main class="mt-200px md:mt-0">
    <Dropdown
    v-model="currentCity"
    title="請選擇縣市"
    :items="dropdownList"
    ></Dropdown>
  </main>
</template>

<script setup>
import { ref, reactive } from "vue";

import Dropdown from "./components/Dropdown.vue";
const dropdownList = [
  {
    label: "台北市",
    value: "01",
  },
  {
    label: "新北市",
    value: "02",
  },
  {
    label: "桃園市",
    value: "03",
  },
  {
    label: "基隆市",
    value: "04",
  },
];

const currentCity = ref("");
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
