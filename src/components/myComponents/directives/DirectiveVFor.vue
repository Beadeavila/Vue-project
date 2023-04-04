<script>
export default {
  data() {
    return {
      title: 'Listado de países',
      list: ['Spain', 'France', 'Italy']
    }
  }
}
</script>
<template>
  <div>
    <h2>Directiva V For: No sirve para recorrer un array, en este caso queremos imprimirlo.</h2>
    <h3>{{ title }}</h3>
    <ul>
      <div v-for="(country, key) in list" :key="key">
        <li :id="[key]">{{ key + 1 }}:{{ country }}</li>
      </div>
    </ul>
  </div>
</template>
<style scoped>
h2 {
  color: blue;
}
</style>
