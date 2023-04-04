<script>
export default {
  data() {
    return {
      comicTitle: 'Amazing Spiderman- Vol.1',
      count: 0
    }
  },
  computed: {
    reversedComicTitle() {
      return this.comicTitle.split('').reverse().join('')
    },
    barColor() {
      return {
        'bg-success': this.count < 20,
        'bg-warning': this.count >= 20 && this.count <= 30,
        'bg-danger': this.count > 30
      }
    }
  }
}
</script>
<template>
  <div>
    <div>
      <h2>
        Propiedades Computadas: se muestran cambios en tiempo real del resultado de las funciones en
        relación a las variables que reciben.
      </h2>
      <p>{{ comicTitle }}</p>
      <p>{{ reversedComicTitle }}</p>
      <input type="text" v-model="comicTitle" />
    </div>
    <div>
      <button class="btn btn-primary" @click="count++">+</button>
      <button class="btn btn-danger" @click="count--">-</button>
      <h3>{{ count }}</h3>

      <div>
        <div
          :class="['progress-bar', barColor]"
          role="progressbar"
          :style="{ width: count + '%' }"
          aria-valuenow="0"
          aria-valuemin="0"
          aria-valuemax="100"
        >
          {{ count }}%
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss">
@import 'bootstrap/dist/css/bootstrap.min.css';
h2 {
  color: blue;
}
</style>
