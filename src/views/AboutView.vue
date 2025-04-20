<template>
  <div class="about">
    <h1>소개 페이지</h1>
    <p>이 사이트는 Vue3의 기본 기능을 소개하기 위해 만들어졌습니다.</p>
    <p>Vue3의 주요 기능:</p>
    <ul>
      <li>Composition API</li>
      <li>더 작은 번들 크기</li>
      <li>향상된 TypeScript 지원</li>
      <li>더 빠른 가상 DOM</li>
      <li>Teleport, Fragments, Suspense 등의 새로운 기능</li>
    </ul>
  </div>
</template>

<style scoped>
.about {
  max-width: 800px;
  margin: 0 auto;
}

h1 {
  color: #343a40;
  margin-bottom: 1rem;
}

p {
  color: #495057;
  line-height: 1.6;
  margin-bottom: 1rem;
}

ul {
  color: #495057;
  line-height: 1.8;
  margin-left: 1rem;
}
</style>
