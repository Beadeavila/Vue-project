<script>
import ComputedProps from '../components/myComponents/computed-properties/ComputedProps.vue'
import DirectiveVFor from '../components/myComponents/directives/DirectiveVFor.vue'
import DirectiveVIf from '../components/myComponents/directives/DirectiveVIf.vue'
import DirectiveVModel from '../components/myComponents/directives/DirectiveVModel.vue'
import DirectiveVShow from '../components/myComponents/directives/DirectiveVShow.vue'
import ParentComponent from '../components/myComponents/props/ParentComponent.vue'
import RawHtmlData from '../components/myComponents/RawHtmlData.vue'
import SingleComponent from '../components/myComponents/SingleComponent.vue'
export default {
  components: {
    SingleComponent,
    RawHtmlData,
    DirectiveVShow,
    DirectiveVIf,
    DirectiveVModel,
    DirectiveVFor,
    ComputedProps,
    ParentComponent
  },
}
</script>
<template>
  <div>
    <h1>My Single Page from FemCoder</h1>
    <h3>Estoy reproduciendo las clases de Vue</h3>
    <SingleComponent />
    <SingleComponent />
    <RawHtmlData />
    <DirectiveVShow />
    <DirectiveVIf />
    <DirectiveVModel />
    <directive-v-for />
    <ComputedProps />
    <ParentComponent />
  </div>
</template>
<style lang="css" scoped>
h1 {
  color: violet;
}
</style>
