<template>
  <form class="searchform" @submit.prevent="onSubmit">
    <input v-model="text" type="text" placeholder="Enter Jokes..." />
    <button type="submit" class="btn-search">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="16"
        height="16"
        fill="currentColor"
        class="bi bi-search"
        viewBox="0 0 16 16"
      >
        <path
          d="M11.742 10.344a6.5 6.5 0 1 0-1.397 1.398h-.001c.03.04.062.078.098.115l3.85 3.85a1 1 0 0 0 1.415-1.414l-3.85-3.85a1.007 1.007 0 0 0-.115-.1zM12 6.5a5.5 5.5 0 1 1-11 0 5.5 5.5 0 0 1 11 0z"
        />
      </svg>
    </button>
  </form>
</template>

<script>
export default {
  name: 'SearchJokes',
  data() {
    return {
      text: '',
    }
  },
  methods: {
    onSubmit() {
      this.$emit('search-text', this.text)
    },
  },
}
</script>

<style scope>
.searchform {
  display: flex;
  align-items: center;
  border: solid 0.0625rem #463742;
  max-width: 18.75rem;
  margin-inline: auto;
  /* border-radius: 1rem; */
  /* height: 2.5rem; */
}

.searchform input {
  width: calc(100% - 2.5rem);
  border: none;
  background: transparent;
  padding: 0.75rem 1rem;
}

input:focus,
textarea:focus {
  outline: none;
}

.btn-search {
  display: flex;
  align-items: center;
  justify-content: center;
  background: #463742;
  width: 2.5rem;
  height: 2.5rem;
  border: none;
  cursor: pointer;
  /* border-radius: 1rem; */
  border: none;
}

.btn-search svg path {
  fill: #ccc;
}
</style>
