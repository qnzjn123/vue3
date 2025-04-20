<template>
  <div class="home">
    <h1>Vue3 기본 사이트에 오신 것을 환영합니다</h1>
    <p>이 사이트는 Vue 3, Vue Router, Pinia를 사용하여 구축되었습니다.</p>
    
    <div class="counter-section">
      <h2>카운터 예제</h2>
      <p>현재 카운트: {{ counter.count }}</p>
      <p>2배 값: {{ counter.doubleCount }}</p>
      <button @click="counter.increment()">증가</button>
    </div>
  </div>
</template>

<script setup>
import { useCounterStore } from '../stores/counter'

const counter = useCounterStore()
</script>

<style scoped>
.home {
  text-align: center;
}

h1 {
  color: #343a40;
  margin-bottom: 1rem;
}

p {
  color: #495057;
  line-height: 1.6;
}

.counter-section {
  margin-top: 2rem;
  padding: 1rem;
  background-color: #f8f9fa;
  border-radius: 0.5rem;
  max-width: 400px;
  margin-left: auto;
  margin-right: auto;
}

button {
  background-color: #4263eb;
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 0.25rem;
  cursor: pointer;
  margin-top: 1rem;
}

button:hover {
  background-color: #3b5bdb;
}
</style>
