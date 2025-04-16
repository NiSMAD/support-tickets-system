<template>
    <span
      :class="{
        'bg-green-100 text-green-800': status === 'решено',
        'bg-red-100 text-red-800': status === 'отклонено',
        'bg-yellow-100 text-yellow-800': status === 'в работе'
      }"
      class="text-xs font-medium px-2 py-1 rounded-lg"
    >
      {{ status }}
    </span>
  </template>
  
  <script>
  export default {
    props: ['status']
  }
  </script>
  