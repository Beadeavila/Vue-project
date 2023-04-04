<script>
export default {
  data() {
    return {
      header: 'Añade tu sabor preferido',
      flavors: []
    }
  }
}
</script>
<template>
  <div>
    <h2>Directiva V Model: Permite cambios en tiempo real</h2>
    <h3>{{ header }}</h3>
    <input type="text" v-model="header" />
    <label>
      <input v-model="flavors" type="checkbox" id="coco" value="coco" name="coco" />Coco
    </label>
    <label>
      <input
        v-model="flavors"
        type="checkbox"
        id="chocolate"
        value="chocolate"
        name="chocolate"
      />Chocolate
    </label>
    <label>
      <input v-model="flavors" type="checkbox" id="fresa" value="fresa" name="fresa" />Fresa
    </label>
    <label>
      <input v-model="flavors" type="checkbox" id="nata" value="nata" name="nata" />Nata
    </label>
  </div>
</template>
<style scoped>
h2 {
  color: blue;
}
</style>
