<template>
 <div>
   <h2>
     this count is: {{counter.oddOrEven}}
   </h2>
   <slot/>
 </div>
</template>
<script setup>
import { useCounterStore } from '@/stores/counter'
const counter = useCounterStore()
</script>
