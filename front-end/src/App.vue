<template>
  <div id="app">
    <Nav></Nav>
    <router-view/>
  </div>
</template>


<script>
import Nav from './components/Nav'
export default {
  name: 'App',
  components: {
    'Nav': Nav
  }
}
</script>

<style lang="scss">
@import './assets/style/reset.scss';
@import './assets/style/app.scss';
</style>
