<script>
export default {
  data() {
    return {
      title: 'El Padrino',
      person: {
        id: 1,
        name: 'Francis Ford Coppola',
        img: 'https://tse2.mm.bing.net/th?id=OIP.Rj0g222VLnCfcYsydyZekgHaEK&pid=Api&P=0',
        msg: 'Al Pacino es el actor principal.'
      }
    }
  }
}
</script>

<template>
  <div v-bind:id="person.name">
    <h2>
      Este componente nos muestra como trabajar con variables(datos metidos en el apartado data del
      script)
    </h2>
    <div>
      <h3>{{ title }}</h3>
      <h4>{{ person.name }}</h4>
      <img :src="person.img" :alt="person.name" />
    </div>
    <h5 v-html="person.msg"></h5>
    <h5>{{ person.msg }}</h5>
  </div>
</template>

<style scoped>
h2 {
  color: blue;
}
h3 {
  text-decoration-line: underline;
}
</style>
