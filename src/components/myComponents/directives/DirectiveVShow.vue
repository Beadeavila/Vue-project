<script>
export default {
  data() {
    return {
      isShowing: true
    }
  },
  methods: {
    changeState() {
      if (this.isShowing) {
        this.isShowing = false
        return
      }
      this.isShowing = true
    }
  }
}
</script>

<template>
  <div>
    <h2>
      Directiva V Show:Nos servirá para decic¡dir si queremos que se muestre o no en la vista algo
      en cuestión
    </h2>
    <button v-on:click="changeState">
      <span v-show="isShowing">Ocultar</span>
    </button>
  </div>
</template>

<style scoped>
h2 {
  color: blue;
}
</style>
