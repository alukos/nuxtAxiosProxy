
<template>
  <div class="container">
    <div>{{ list }}</div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData({ req, params }) {
    let { data } = await axios.get('/depth/ltc_btc-nmc_btc')
    return { list: data};
  },
  head: {
    title: 'List'
  }
}
</script>