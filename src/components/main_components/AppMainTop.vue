<script >
export default {
    name: "AppMainTop"
}
</script>

<template>
    <div class="count_bar">
        <h3>Found 100 elements</h3>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/variables' as*;

.count_bar {
    background-color: $tertiary;
    padding: 15px;
    margin-bottom: 50px;
}
</style>
