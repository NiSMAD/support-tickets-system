<template>
    <div class="bg-white rounded-xl shadow-md p-6">
      <h2 class="text-2xl font-semibold text-slate-800 mb-4">Текущие заявки</h2>
  
      <div v-if="tickets.length === 0" class="text-slate-500 italic">Пока нет заявок</div>
  
      <div v-for="ticket in tickets" :key="ticket.id" class="p-4 mb-4 border border-slate-200 rounded-lg bg-slate-50">
        <div class="flex justify-between items-center mb-2">
          <h3 class="text-lg font-semibold text-slate-700">{{ ticket.title }}</h3>
          <TicketStatus :status="ticket.status" />
        </div>
        <p class="text-slate-600 text-sm">{{ ticket.desc }}</p>
      </div>
    </div>
  </template>
  
  <script>
  import TicketStatus from './TicketStatus.vue'
  export default {
    props: ['tickets'],
    components: { TicketStatus }
  }
  </script>
  