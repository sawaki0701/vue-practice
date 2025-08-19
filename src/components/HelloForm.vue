<template>
  <div>
    <h2>名前を入力してください</h2>
    <input v-model="name" placeholder="名前" />
    <button @click="submit">送信</button>
    <div v-if="submitted">
      <h3>入力された名前リスト</h3>
      <ul>
        <li v-for="(user, index) in users" :key="index">{{ user }}</li>
      </ul>
    </div>
  </div>
</template>
<script setup lang="ts">
import { ref } from 'vue'
const name = ref('')
const submitted = ref(false)
const users = ref<string[]>([])
const submit = () => {
  if (name.value.trim() === '') return
  users.value.push(name.value)
  name.value = ''
  submitted.value = true
}
</script>
<style scoped>
input {
  margin-right: 10px;
  padding: 4px 6px;
}
button {
  padding: 4px 8px;
}
</style>
