<template>
  <div>
    <h3>{{ user.first_name }} {{ user.last_name }}</h3>
    <p>{{ user.email }}</p>
  </div>
</template>

<script>
export default {
  props: {
    user: Object
  }
}
</script>
