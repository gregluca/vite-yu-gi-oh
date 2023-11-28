<script>
import { store } from "../store";

export default {
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div class="container">
    <h2> Totale {{ store.cards.data.length }} personaggi </h2>
  </div>
</template>
<style scoped lang="scss">
h2 {
  color: white;
}
</style>