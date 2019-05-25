<template>
  <section class="container">
    <div>
      <!-- 會創造全新的一頁，跳脫SPA，並對server發出新的request，css樣式也不會吃到SPA全域的樣式 -->
      <a href="/users">Users(a)</a><br>
      <!--原有的SPA下去做routing，底層使用vue router -->
      <nuxt-link to="/users">Users(nuxt-link)</nuxt-link><br>
      <button @click="$router.push('/products')">Go to Products Page</button>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
h1 {
  color: red;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
