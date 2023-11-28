<script>

export default {
    props : {
        card: Object,
    }
}
</script>

<template>
    <div class="custom-card  h-100 ">
        <img :src="card.card_images[0].image_url" alt="">
        <h6 class="text-center my-3">{{ card.name }}</h6>
        <p class="text-center">{{ card.archetype }}</p>
    </div>
</template>

<style scoped lang="scss">
img {
    max-width: 100%;
}
.custom-card {
    background-color: orange;
}
</style>