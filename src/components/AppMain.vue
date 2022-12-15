<script >
import AppMainTop from './main_components/AppMainTop.vue';
import AppMainCardList from './main_components/AppMainCardList.vue';

export default {
    name: "AppMain",
    components: {
        AppMainTop,
        AppMainCardList,
    }
}
</script>

<template>
    <!-- container -->
    <div class="container">
        <AppMainTop />
        <AppMainCardList />
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.container {
    max-width: 1200px;
    margin: 50px auto;
    padding: 30px;
    background-color: $secondary;
}
</style>
