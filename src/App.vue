<script>
import axios from "axios";
import { store } from "./store.js";
import AppHeader from "./components/AppHeader.vue";
import AppList from "./components/AppList.vue";
import AppSelect from "./components/AppSelect.vue";


export default {
  data () {
    return {
      store
    };
    
  },
  created() {
    axios
    .get(this.store.apiUrl, {
      params: {
        num: 20,
        offset: 0
      }
    })
    .then((resp) => {
      this.store.cards = resp.data;
    });
  },
  methods: {
    handleSearch(){
      axios
      .get(this.store.apiArchUrl, {
        params: {
          archetype: this.store.selectOption,
          num: 20,
          offset: 0
        }
      }).then((resp) => {
        this.store.cards = resp.data;
      })
    }
  },
  components: { AppHeader, AppList, AppSelect }
}

</script>

<template>

<AppHeader />
<AppSelect @show="handleSearch" />
<AppList />

</template>

<style lang="scss">
@use "./style/general.scss";
</style>