<template>
  <button id="filterButton">{{ title }}</button>
</template>

<script>
export default {
  name: "filterBtn",
  props: {
    title: String,
  },
};
</script>

<style scoped>
button {
  margin-right: 26px;
  height: 45px;
  width: 130px;
  left: 0px;
  top: 0px;
  border-radius: 100px;
  background-color: #d9d9d900;
  border: 0.5px solid #686868;
  font-family: "Inter";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 16px;
}
button:hover {
  background-color: #d9d9d986;
}
</style>