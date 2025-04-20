<template>
  <div class="contact">
    <h1>연락처</h1>
    <p>궁금한 사항이 있으시면 아래 양식을 통해 문의해주세요.</p>
    
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">이름</label>
        <input type="text" id="name" v-model="form.name" required>
      </div>
      
      <div class="form-group">
        <label for="email">이메일</label>
        <input type="email" id="email" v-model="form.email" required>
      </div>
      
      <div class="form-group">
        <label for="message">메시지</label>
        <textarea id="message" v-model="form.message" rows="5" required></textarea>
      </div>
      
      <button type="submit">제출하기</button>
    </form>
    
    <div v-if="submitted" class="success-message">
      메시지가 성공적으로 전송되었습니다!
    </div>
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

const form = reactive({
  name: '',
  email: '',
  message: ''
})

const submitted = ref(false)

const submitForm = () => {
  // 여기서 실제로는 API로 폼 데이터를 전송합니다
  console.log('Form submitted:', form)
  
  // 폼 제출 성공 메시지 표시
  submitted.value = true
  
  // 폼 초기화
  form.name = ''
  form.email = ''
  form.message = ''
  
  // 3초 후 성공 메시지 숨기기
  setTimeout(() => {
    submitted.value = false
  }, 3000)
}
</script>

<style scoped>
.contact {
  max-width: 600px;
  margin: 0 auto;
}

h1 {
  color: #343a40;
  margin-bottom: 1rem;
}

p {
  color: #495057;
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.form-group {
  margin-bottom: 1rem;
}

label {
  display: block;
  margin-bottom: 0.5rem;
  color: #495057;
}

input, textarea {
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #ced4da;
  border-radius: 0.25rem;
}

button {
  background-color: #4263eb;
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 0.25rem;
  cursor: pointer;
}

button:hover {
  background-color: #3b5bdb;
}

.success-message {
  margin-top: 1rem;
  padding: 0.75rem;
  background-color: #d4edda;
  color: #155724;
  border-radius: 0.25rem;
  text-align: center;
}
</style>
