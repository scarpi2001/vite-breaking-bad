<script >
export default {
    name: "AppMainCard",
    props: {
        details: Object
    }
}
</script>

<template>
    <!-- card -->
    <div class="card">
        <figure>
            <img :src="details.image" :alt="details.name">
        </figure>

        <h3>{{ details.name }}</h3>
        <div class="text">{{ details.status }}</div>
        <div class="text">{{ details.species }}</div>
        <div class="text">{{ details.gender }}</div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/variables' as*;

.card {
    width: calc(100% / 3 - 40px);
    padding: 20px;
    margin: 0 20px;
    margin-bottom: 30px;
    text-align: center;
    background-color: $primary;
    border-radius: 20px;

    figure {
        margin-bottom: 15px;


        img {
            border-radius: 20px;
        }
    }

    .text {
        margin-bottom: 5px;
    }
}
</style>
