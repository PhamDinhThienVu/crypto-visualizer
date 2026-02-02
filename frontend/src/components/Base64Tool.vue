<template>
  <div class="base64-tool">
    <h2>Base64 Encode/Decode</h2>
    <textarea v-model="inputText" placeholder="Nhập text tại đây"></textarea>
    
    <div class="buttons">
      <button @click="encodeBase64">Encode</button>
      <button @click="decodeBase64">Decode</button>
    </div>

    <div class="result">
      <h3>Kết quả:</h3>
      <pre>{{ result }}</pre>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'Base64Tool',
  setup() {
    const inputText = ref('')
    const result = ref('')

    const encodeBase64 = () => {
      result.value = btoa(inputText.value)
    }

    const decodeBase64 = () => {
      try {
        result.value = atob(inputText.value)
      } catch (e) {
        result.value = '❌ Lỗi: chuỗi không hợp lệ cho Base64'
      }
    }

    return { inputText, result, encodeBase64, decodeBase64 }
  }
})
</script>

<style scoped>
.base64-tool {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
textarea {
  width: 100%;
  height: 100px;
}
.buttons {
  display: flex;
  gap: 1rem;
}
.result {
  background: #f5f5f5;
  padding: 1rem;
  border-radius: 5px;
}
</style>
