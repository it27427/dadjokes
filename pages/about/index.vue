<template>
  <div>
    <h2 class="title">About DadJokes</h2>
    <p>This is an app that displays corny dad jokes</p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'About The App',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for corny dad jokes',
        },
      ],
    }
  },
}
</script>
