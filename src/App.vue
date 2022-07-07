<template>
  <div id="app">
    <DcHeader />

    <DcJumbotron />

    <DcMain />

    <DcFooter />

  </div>
</template>

<script>
import DcHeader from './components/DcHeader.vue'
import DcJumbotron from './components/DcJumbotron.vue'
import DcMain from './components/DcMain.vue'
import DcFooter from './components/DcFooter.vue'

export default {
  name: 'App',
  components: {
    DcHeader,
    DcJumbotron,
    DcMain,
    DcFooter
  }
}
</script>

<style lang="scss">
@import './style/common';
</style>
