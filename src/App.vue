<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <div class="app">
    <!-- ここに共通レイアウトを持たせる -->
    <header class="header">
      <h1>My Vue App</h1>
    </header>

    <main class="main">
      <!-- 現在のルートのコンポーネントを表示 -->
      <RouterView />
    </main>
  </div>
</template>

<style scoped>
.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 0;
  padding: 0;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.header {
  background-color: #42b983; /* Vueっぽい緑色 */
  color: white;
  text-align: center;
  padding: 1rem;
}

.main {
  flex: 1;
  padding: 2rem;
}

.footer {
  background-color: #f5f5f5;
  text-align: center;
  padding: 0.5rem;
  font-size: 0.8rem;
  color: #555;
}
</style>
