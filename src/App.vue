<template>
  <div id="app">
      <router-view/>
      <Footer />
  </div>
</template>

<script>
import Footer from '@/components/layouts/Footer';

export default {
  components: {
    Footer,
  }
}
</script>

<style>
  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: 'Open Sans', sans-serif;
  }

  body {
    background: #1A202C;
  }
</style>