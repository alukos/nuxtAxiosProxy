
<template>
  <div class="container">
    <div>{{ list }}</div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  async asyncData(context) {
    let { data } = await axios.get(
      "https://yobit.net/api/3/depth/ltc_btc-nmc_btc"
    );
    return { list: data };
  },
  head: {
    title: "List",
  },
};
</script>
