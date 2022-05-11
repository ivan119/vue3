<template>
  <div class="about">
    <h1>About</h1>
    <h1 class="num" @click="counter.increaseCount" @mouseleave="counter.decreaseCount">
      {{counter.count}}
    </h1>
    <count-component >
      <div style="border: 1px solid black; border-radius: 7px; margin: 0px 40px">
        <h3>slot test</h3>
        <img style="width:100%" src="https://vuejs.org/assets/slots.dbdaf1e8.png" alt="">
      </div>
    </count-component>

  </div>
</template>

<script setup>
import  countComponent from '@/components/Counter.vue'
import { useCounterStore } from '@/stores/counter'
const counter = useCounterStore()
</script>

<style  scoped>
.num {
  border: 1px solid gray;
  border-radius: 7px;
  margin: auto;
  padding: 2px;
  width: 40px;
  cursor: pointer;
}
</style>
