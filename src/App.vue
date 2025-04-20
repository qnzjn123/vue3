<template>
  <header>
    <nav>
      <router-link to="/">홈</router-link>
      <router-link to="/about">소개</router-link>
      <router-link to="/contact">연락처</router-link>
    </nav>
  </header>

  <main>
    <router-view />
  </main>

  <footer>
    <p>&copy; 2023 Vue3 기본 사이트</p>
  </footer>
</template>

<style>
header {
  padding: 1rem;
  background-color: #f8f9fa;
  border-bottom: 1px solid #e9ecef;
}

nav {
  display: flex;
  gap: 1rem;
}

nav a {
  color: #495057;
  text-decoration: none;
  padding: 0.5rem 1rem;
  border-radius: 0.25rem;
  transition: background-color 0.3s;
}

nav a:hover {
  background-color: #e9ecef;
}

nav a.router-link-active {
  color: #4263eb;
  font-weight: bold;
}

main {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

footer {
  text-align: center;
  padding: 1rem;
  background-color: #f8f9fa;
  border-top: 1px solid #e9ecef;
  margin-top: 2rem;
}
</style>
