<template>
  <section class="container">
    <div>
      <h1>User id : {{ $route.params.id }}</h1>
    </div>
  </section>
</template>

<script>

export default {
  validate(data) {
    console.log(data)
    return /^\d+$/.test(data.params.id) //可以用來驗證param是數字才進來
    // return data.params.id === '1'
  }
}
</script>