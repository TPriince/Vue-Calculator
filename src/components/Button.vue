<template>
  <button @click="method" :class="class">{{ value }}</button>
</template>

<script>
  export default {
    name: "Button",
    props: {
      value: String,
      class: String,
      method: { type: Function }
    },
  }
</script>

<style>
button {
  width: 25%;
  height: 50px;
  border: 1px solid white;
  background-color: black;
  color: white;
  transition: all 1s;
  font-weight: 700;
} 
</style>