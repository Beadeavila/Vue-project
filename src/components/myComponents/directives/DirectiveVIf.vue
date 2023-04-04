<script>
export default {
  data() {
    return {
      movies: [],
      newTitle: '',
      adding: false
    }
  },
  methods: {
    addMovie() {
      this.movies.push({
        id: this.movies.length + 1,
        title: this.newTitle
      })
      this.newTitle = ''
    },
    showInputToAdd(state) {
      this.adding = state
      this.newTitle = ''
    }
  }
}
</script>
<template>
  <div>
    <h2>
      Directivas V If y V Else: Permiten establecer condiciones para realizar acciones determinadas
    </h2>
    <label class="m-3">Testing directive v-if and v-else</label>
    <button v-if="adding == false" v-on:click="showInputToAdd(true)">Add Movie</button>
    <button v-else v-on:click="showInmputToAdd(false)">Cancel</button>
    <div v-if="adding">
      <input
        id="add-movie-input"
        @keyup.enter="addmovie()"
        v-model="newTitle"
        placeholder="Add a movie"
      />
      <button v-on:click="addMovie()" class="btn btn-primary">+</button>
    </div>
    <span v-if="movies.length == 0" class="m-3">Please add Movie</span>
    <ul class="m-3">
      <div v-for="(movie, key) in movies" :key="movie.id">
        <li :id="key">{{ movie.id }}:{{ movie.title }}</li>
      </div>
    </ul>
  </div>
</template>
<style scoped>
h2 {
  color: blue;
}
</style>
