<template>
  <div class="users-wrapper">
    <h1>this is users page</h1>
    <input type="text" v-model="userId">
    <button @click="onLoadUser">Load User</button>
    <nuxt-child />
  </div>
</template>

<script>

export default {
  data() {
    return {
      userId: ''
    }
  },
  methods: {
    onLoadUser() {
      this.$router.push(`/users/${this.userId}`)
    }
  },
  layout: 'users'
}
</script>

<style>
  .users-wrapper {
    padding: 100px;
    margin: 0 auto;
    text-align: center;
  }
</style>