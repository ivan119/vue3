<template>
  <div class="home">
    <h1>{{counter.count}}</h1>
    <count-component />
    <div class="buttons">
      <button @click="counter.decreaseCount">-</button>
      <button @click="counter.increaseCount">+</button>
    </div>
    <hr>
    <div>
      <h3>Two way binding</h3>
      <input type="number" placeholder="Change counter" v-model="counter.count" min="0">
    </div>
  </div>
</template>
<script setup>
import  countComponent from '@/components/Counter.vue'
import {useCounterStore} from "@/stores/counter";
const counter = useCounterStore()
</script>
<style>
.counter{
  font-size: 63px;
  margin: 23px
}
.buttons button {
  font-size: 43px;
  margin: 12px;
  cursor: pointer;
  background: white;
  border: 1px solid goldenrod;
  border-radius: 3px;
  padding: 3px 23px;
  transition: background-color ease-in-out 200ms;
}
.buttons button:hover {
  background: goldenrod;
}
</style>
