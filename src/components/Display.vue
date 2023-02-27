<template>
  <div :class="class">{{ value }}</div>
</template>

<script>
export default {
  name: "Display",
  props: {
    value: String,
    class: String
  }
}
</script>

<style>
div.display {
  background-color: white;
  width: 100%;
  height: 120px;
  margin-bottom: 10px;
  border: 5px inset grey;
  border-radius: 6px;
  font-size: xx-large;
  text-align: right;
  padding: 10px;
  word-wrap: break-word;
}
</style>