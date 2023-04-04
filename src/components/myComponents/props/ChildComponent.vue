<script>
import { stringifyExpression } from '@vue/compiler-core'

export default {
  props: {
    movieTitle: String,
  },
  data(){
    return{
      brand: 'DC Comics',
    }
  },
  methods:{
    sendBrand(){
      this.$emit('brand',this.brand)
    }
  }
  
}
</script>
<template>
  <h2>Hijita</h2>
  <h2>{{ movieTitle }}ita</h2>
  <button @click = "sendBrand">Send Brand</button>
</template>
