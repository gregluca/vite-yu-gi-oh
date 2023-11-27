<script>
import { store } from "../store";
import AppCard from './AppCard.vue';

export default {
    data() {
        return {
            store,
        };
    },
    components: { AppCard }
}
</script>

<template>
 <div class="container">
        <div class="row ">
            <div class="col-3 align-items-stretch" v-for="card in store.cards" :key="card.id">
                <AppCard :card="card" />
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">

</style>