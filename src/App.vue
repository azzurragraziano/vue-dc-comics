<template>
  <div id="app">
    <DcHeader />

    <DcMain />

  </div>
</template>

<script>
import DcHeader from './components/DcHeader.vue'
import DcMain from './components/DcMain.vue'

export default {
  name: 'App',
  components: {
    DcHeader,
    DcMain
  }
}
</script>

<style lang="scss">
@import './style/common';
</style>
