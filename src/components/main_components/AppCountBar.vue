<script >
import { store } from '../../store';

export default {
    name: "AppCountBar",
    data() {
        return {
            store,
        }
    },
}
</script>

<template>
    <!-- count bar -->
    <div class="count_bar">
        <h3>trovati {{ store.characterList.length }} elementi</h3>
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
