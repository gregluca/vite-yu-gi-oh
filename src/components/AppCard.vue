<script>
export default {
    props : {
        card: Object,
    },
};
</script>

<template>
    <div class="custom-card h-100">
        <img :src="card.card_images[0].image_url_small" alt="">
        <h6 class="text-center my-3">{{ card.name }}</h6>
        <p class="text-center">{{ card.archetype ? card.archetype : "Nessun archetipo" }}</p>
    </div>
</template>

<style scoped lang="scss">

.custom-card {
    text-align: center;
    padding-top: 1rem;
    background-color: orange;
    color: white;
}
</style>