<template>
    <div class="min-h-screen bg-slate-100 p-6">
      <div class="max-w-4xl mx-auto">
        <h1 class="text-4xl font-bold text-slate-800 mb-4">Система заявок ТП</h1>
        <p class="text-slate-500 mb-8">Создавай, отслеживай и управляй заявками прямо здесь.</p>
  
        <TicketForm @new-ticket="addTicket" />
        <TicketTable :tickets="tickets" />
      </div>
    </div>
  </template>
  
  <script>
  import TicketForm from './components/TicketForm.vue'
  import TicketTable from './components/TicketTable.vue'
  
  export default {
    components: { TicketForm, TicketTable },
    data() {
      return {
        tickets: []
      }
    },
    methods: {
      addTicket(ticket) {
        this.tickets.unshift({ ...ticket, status: 'в работе', id: Date.now() })
      }
    }
  }
  </script>
  