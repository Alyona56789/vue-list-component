<template>
  <div id="app">
    <header class="header">
      <h1>👥 Список сотрудников</h1>
      <p>Всего пользователей: {{ users.length }}</p>
    </header>
    <main class="list-container">
      <ListItem 
        v-for="user in users" 
        :key="user.id" 
        :user="user" 
      />
    </main>
  </div>
</template>

<script>
import ListItem from './components/ListItem.vue'
import usersData from './data/users.json'

export default {
  name: 'App',
  components: { ListItem },
  data() {
    return { users: usersData }
  }
}
</script>

<style>
/* Сброс стандартных отступов */
* { box-sizing: border-box; margin: 0; padding: 0; }
body { font-family: system-ui, -apple-system, sans-serif; background: #f5f7fa; }

#app { max-width: 800px; margin: 0 auto; background: #fff; min-height: 100vh; box-shadow: 0 2px 10px rgba(0,0,0,0.05); }

.header { background: #42b983; color: white; padding: 20px; text-align: center; }
.header h1 { font-size: 24px; margin-bottom: 5px; }
.header p { font-size: 14px; opacity: 0.9; }

.list-container { padding: 20px; }
</style>