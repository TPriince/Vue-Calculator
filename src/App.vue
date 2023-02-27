<template>
  <div class="container">
    <Display class="display" :value="num"/>
    
    <Button class="button clear" value="C" :method="handleClear" />
    <Button class="button" value="%" :method="handlePercentage" />
    <Button class="button op" value="/" :method="handleClick" />
    <Button class="button" value="7" :method="handleClick" />
    <Button class="button" value="8" :method="handleClick" />
    <Button class="button" value="9" :method="handleClick" />
    <Button class="button op" value="*" :method="handleClick" />
    <Button class="button" value="4" :method="handleClick" />
    <Button class="button" value="5" :method="handleClick" />
    <Button class="button" value="6" :method="handleClick" />
    <Button class="button op" value="-" :method="handleClick" />
    <Button class="button" value="1" :method="handleClick" />
    <Button class="button" value="2" :method="handleClick" />
    <Button class="button" value="3" :method="handleClick" />
    <Button class="button op" value="+" :method="handleClick" />
    <Button class="button" value="0" :method="handleClick" />
    <Button class="button" value="." :method="handleClick" />
    <Button class="button" value="del" :method="handleDelete" />
    <Button class="button op equalto" value="=" :method="handleResult" />
  </div>
    
</template>

<script>
import Button from "./components/Button.vue"
import Display from "./components/Display.vue"
export default {
  name: "App",
  components: {
    Button,
    Display
  },
  data () {
    return {
      num: ""
    }
  },
  methods: {
    handleClick(e) {
      if (this.num.length > 14 ) {
        alert("Can't enter more than 15 digits.");
      } else {
        this.num = this.num + e.target.textContent;
      }
  },
    handleClear(e) {
      this.num = "";
  },
    handleDelete() {
      this.num = this.num.slice(0, this.num.length - 1);
  },
    handlePercentage() {
      this.num = (eval(this.num) / 100).toString();
  },
    handleResult() {
      this.num = eval(this.num).toString();
    }
}
}
</script>
 
<style>
.container {
  padding: 20px;
  max-width: 280px;
  border: 1px solid black;
  border-radius: 4px;
  margin: 50px auto;
  box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
}

.clear {
  width: 50%;
}

.button:hover {
  background-color: white;
  color: black;
  font-weight: 700;
  border: 1px solid black;
}

.op {
  background-color: blueviolet;
  color: black;
}

.equalto {
  background-color: gold;
}
</style>
