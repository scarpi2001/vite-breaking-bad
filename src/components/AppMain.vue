<script >
import AppMainTop from './main_components/AppMainTop.vue';

export default {
    name: "AppMain",
    components: {
        AppMainTop
    }
}
</script>

<template>
    <div class="container">
        <AppMainTop />
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.container {
    max-width: 1000px;
    margin: 50px auto;
    padding: 30px;
    background-color: $secondary;
}
</style>
