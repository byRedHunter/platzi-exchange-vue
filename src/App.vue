<template>
  <main>
    <px-header />

    <div class="contenedor">
      <router-view class="container mt-20" />
    </div>
  </main>
</template>

<script>
import PxHeader from '@/components/PxHeader'

export default {
  name: 'app',
  components: {
    PxHeader
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.contenedor {
  max-width: 1000px;
  width: 90%;
  margin: 0 auto;
  overflow: hidden;
}
</style>
