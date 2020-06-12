<template>
  <main>
    <px-header :links="links" />

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
  },

  data() {
    return {
      links: [
        {
          title: 'BTC',
          to: { name: 'coin-detail', params: { id: 'bitcoin' } }
        },
        {
          title: 'ETH',
          to: { name: 'coin-detail', params: { id: 'ethereum' } }
        },
        {
          title: 'XRP',
          to: { name: 'coin-detail', params: { id: 'ripple' } }
        }
      ]
    }
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
