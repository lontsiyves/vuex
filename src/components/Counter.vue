<template>
  <div>
    <h1 class="title">VueX counter</h1>
    <h1 class="counter">{{ counter }}</h1>
    <div class="counter-board">
      <button  @click="subTraction(parseInt(value))"  class="btn-opt">-</button>
      <input v-model="value" type="number" />
      <button @click="addToCounter(parseInt(value))" class="btn-opt">+</button>
      <div>
          <button class="btn" @click="addRandomNumber">Add By Random number</button>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState, mapMutations, mapActions } from 'vuex';
export default {
  data() {
    return {
      value: 1,
    };
  },
  computed: {
      ...mapState(['counter'])
  },
  methods: {
      ...mapMutations(['addToCounter', 'subTraction']),
      ...mapActions(['addRandomNumber'])
  }
};
</script>
<style scoped>
.counter {
  font-size: 5rem;
}
.title {
  margin-bottom: 50px;
}
.counter-board {
  display: flex;
  text-align: center;
  justify-content: center;
  align-items: center;
}
.btn-opt {
  border-radius: 100%;
  border: none;
  width: 2rem;
  cursor: pointer;
  font-weight: 700;
}
input {
  padding: 0.4rem;
  margin: 0 0.5rem;
  text-align: center;
}
.btn {
border-radius: 0.5rem;
width: auto;
background-color:  #41b983;
color: #fff;
}
</style>
