<script>
import axios from "axios";
import { store } from "./store.js";
import AppHeader from "./components/AppHeader.vue";
import AppList from "./components/AppList.vue";

export default {
  data () {
    return {
      store
    };
    
  },
  created() {
    axios.get(this.store.apiUrl).then((resp) => {
      this.store.cards = resp.data.data;
    });
  },
  components: { AppHeader, AppList }
}

</script>

<template>

<AppHeader />
<AppList />

</template>

<style lang="scss">
@use "./style/general.scss";
</style>