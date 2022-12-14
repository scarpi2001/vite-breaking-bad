<script >
export default {
    name: "AppMainCard",
}
</script>

<template>
    <!-- card -->
    <div class="card">
        <figure>
            <img :src="details.thumb" :alt="details.series">
        </figure>

        <span>{{ details.series }}</span>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/variables' as*;

.card {
    width: calc(100% / 6 - 40px);
    margin: 0 20px;
    margin-bottom: 30px;

    figure {
        height: 150px;
        margin-bottom: 15px;
        overflow: hidden;
    }

    span {
        font-size: 18px;
    }

}
</style>
