<template>
  <div class="card">
    <img :src="user.avatar" :alt="user.first_name" class="avatar" />
    <div class="info">
      <h3>{{ user.first_name }} {{ user.last_name }}</h3>
      <p class="email">📧 {{ user.email }}</p>
      <p class="job">💼 {{ user.job_title }}</p>
      <p class="id">🔢 ID: {{ user.id }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ListItem',
  props: {
    user: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.card {
  display: flex;
  align-items: center;
  gap: 15px;
  padding: 15px;
  border-bottom: 1px solid #eee;
  transition: background-color 0.2s;
}
.card:hover { background-color: #f9f9f9; }
.avatar {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  object-fit: cover;
  flex-shrink: 0;
}
.info h3 { margin: 0 0 4px; font-size: 16px; color: #333; }
.email { margin: 0 0 4px; color: #666; font-size: 13px; }
.job { margin: 0 0 4px; color: #888; font-size: 12px; text-transform: uppercase; letter-spacing: 0.5px; }
.id { margin: 0; color: #aaa; font-size: 11px; font-family: monospace; }
</style>