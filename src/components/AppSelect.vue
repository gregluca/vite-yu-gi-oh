<script>
import { store } from '../store';

export default {
    data() {
        return {
            store,
        }
    }
}
</script>
<template>
    <div class="container">
        <select class="form-select w-25" v-model="store.selectOption" @change="$emit('show')">
            <option value="Alien">Alien</option>
            <option value="Ally of Justice">Ally of Justice</option>
            <option value="Ancient Gear">Ancient Gear</option>
        </select>
    </div>
</template>

<style scoped lang="scss">
.container {
    padding: 2rem;
    display: flex;
    justify-content: center;
}
</style>