<template>
  <div>
    <search-jokes @search-text="searchText" />
    <single-joke
      v-for="joke in jokes"
      :id="joke.id"
      :key="joke.id"
      :joke="joke.joke"
    />
  </div>
</template>

<script>
import axios from 'axios'
import SingleJoke from '@/components/SingleJoke'
import SearchJokes from '@/components/SearchJokes'

export default {
  components: {
    SingleJoke,
    SearchJokes,
  },
  data() {
    return {
      jokes: [],
    }
  },
  head() {
    return {
      title: 'Dad Jokes',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for corny dad jokes',
        },
      ],
    }
  },
  async created() {
    const config = {
      headers: {
        Accept: 'application/json',
      },
    }

    try {
      const res = await axios.get('https://icanhazdadjoke.com/search', config)

      this.jokes = res.data.results
    } catch (err) {
      console.error(err)
    }
  },
  methods: {
    async searchText(text) {
      const config = {
        headers: {
          Accept: 'application/json',
        },
      }

      try {
        const res = await axios.get(
          `https://icanhazdadjoke.com/search?term=${text}`,
          config
        )

        this.jokes = res.data.results
      } catch (err) {
        console.error(err)
      }
    },
  },
}
</script>
