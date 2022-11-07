<template>
  <header class="header">
    <h1 class="title">Dad Jokes</h1>
    <ul>
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/jokes">Jokes</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
}
</script>

<style>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  margin-bottom: 1rem;
  padding-bottom: 1rem;
  border-bottom: dashed 0.0625rem #ccc;
}

@media screen and (max-width: 33.75rem) {
  .header {
    justify-content: center;
  }
}

.header .title {
  color: #526488;
  font-size: 3rem;
}

.header ul {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.header ul a {
  background: #333;
  color: #eee;
  display: inline-block;
  padding: 0.3rem 1rem;
}
</style>
