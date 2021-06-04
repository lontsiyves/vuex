<template>
  <div>
    Component1
  </div>
  <Component2 />
</template>

<script>
import Component2 from './Component2';

export default {
  components: {
     Component2
  }
}
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
