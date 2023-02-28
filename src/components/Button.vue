<template>
  <button @click="handleClick" :class="class">{{ value }}</button>
</template>

<script>
  export default {
    name: "Button",
    props: {
      value: String,
      class: String,
    },
    methods: {
      handleClick(e) {
        this.$emit('btn-click', e.target.textContent)
      }
    }
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