<script setup lang="ts">
import instance from '../api/axios'
async function onClick() {
  alert('클릭')
  try {
    const response = await instance.get('/api/example-endpoint')
    // const response = await axios.get<string>('/example-endpoint')
    alert(response.data)
  } catch (error) {
    console.error('Error fetching data:', error)
  }
}
</script>

<template>
  <main>
    여기는 메인입니다.
    <button @click="onClick">클릭!!</button>
  </main>
</template>
