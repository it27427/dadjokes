<template>
  <nuxt-link :to="'jokes/' + id">
    <div class="joke">
      <p>{{ joke }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: 'SingleJoke',
  props: ['joke', 'id'],
}
</script>

<style>
.joke {
  padding: 1rem;
  border: dotted 0.0625rem #ccc;
  margin: 1rem 0;
}
</style>
