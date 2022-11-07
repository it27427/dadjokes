<template>
  <div class="container">
    <AppHeader />
    <Nuxt />
  </div>
</template>

<script>
import AppHeader from '../components/AppHeader'

export default {
  components: {
    AppHeader,
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=PT+Sans&family=Poor+Story&display=swap');

html {
  font-size: 100%;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: inherit;
}

body {
  background: #f4f4f4;
  font-family: 'PT Sans', sans-serif;
  font-size: 1rem;
  font-weight: normal;
  line-height: 1.4;
  margin: 0;
  overflow-x: hidden;
}

h1,
h2,
h3,
h4,
h5,
h6,
p,
section,
figure {
  margin: 0;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: 'Poor Story', cursive;
}

ul {
  list-style: none;
}

a {
  text-decoration: none;
  color: #666;
}

a,
li,
span,
p,
div,
section,
article {
  font: inherit;
}

.container {
  background: white;
  max-width: 50rem;
  margin: 2rem auto;
  overflow: hidden;
  padding: 1rem 2rem;
}
</style>
