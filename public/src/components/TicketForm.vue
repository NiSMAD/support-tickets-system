<template>
    <form @submit.prevent="submit" class="mb-6 bg-white p-6 rounded-xl shadow-md space-y-4">
      <div>
        <label class="block text-sm font-medium text-slate-700 mb-1">Заголовок</label>
        <input v-model="title" class="input-field" placeholder="Введите тему заявки" />
      </div>
      <div>
        <label class="block text-sm font-medium text-slate-700 mb-1">Описание</label>
        <textarea v-model="desc" class="input-field h-24" placeholder="Опишите проблему..."></textarea>
      </div>
      <button class="bg-indigo-600 text-white px-5 py-2 rounded-lg hover:bg-indigo-700 transition">
        Отправить заявку
      </button>
    </form>
  </template>
  
  <script>
  export default {
    data() {
      return { title: '', desc: '' }
    },
    methods: {
      submit() {
        if (this.title && this.desc) {
          this.$emit('new-ticket', { title: this.title, desc: this.desc })
          this.title = ''
          this.desc = ''
        }
      }
    }
  }
  </script>
  
  <style scoped>
  .input-field {
    width: 100%;
    padding: 0.5rem 0.75rem;
    border: 1px solid #cbd5e1;
    border-radius: 0.5rem;
    font-size: 0.95rem;
    background-color: #f8fafc;
    transition: border-color 0.2s;
  }
  .input-field:focus {
    outline: none;
    border-color: #6366f1;
  }
  </style>
  