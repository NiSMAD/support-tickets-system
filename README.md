# Support Ticket Management Interface

![Vue](https://img.shields.io/badge/Vue-3-green)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.3-blue)
![Vite](https://img.shields.io/badge/Vite-4.x-orange)

A simple and intuitive interface for handling support tickets, built with Vue 3 and Tailwind CSS.

## 🧠 Features

- **Create New Tickets**  
  Submit tickets with title and description
- **Track Status**  
  Clear status indicators: `In Progress` | `Resolved` | `Needs Improvement`
- **Ticket History**  
  Tabular view of all requests with sorting
- **Responsive Design**  
  Works on all device sizes

## 🛠️ Tech Stack

- **Framework**: [Vue 3](https://vuejs.org/) (Composition API)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Build Tool**: [Vue](https://vuejs.org/)

## 🚀 Quick Start

```bash
# 1. Clone repository
git clone https://github.com/yourusername/support-tickets.git

# 2. Install dependencies
npm install

# 3. Run development server
npm run dev
```

## 📂 Project Structure
```
/src
├── /assets           # Static files
├── /components       # Reusable components
│   ├── TicketForm.vue
│   └── TicketList.vue
├── /stores           # State management
│   └── tickets.js
├── /views            # Page components
│   ├── Dashboard.vue
│   └── TicketView.vue
├── App.vue           # Main component
└── main.js           # Entry point
```

> [!NOTE]
> ℹ️ This project was created during my initial Vue.js learning phase. While functional, it represents early work with the framework and may contain simplification
