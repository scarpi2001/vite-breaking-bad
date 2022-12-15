<script >
import AppMainCard from './AppMainCard.vue';

import { store } from '../../store';

export default {
    name: "AppMainCardList",
    components: {
        AppMainCard,
    },
    data() {
        return {
            store,
        }
    },
}
</script>

<template>
    <!-- contenitore cards -->
    <div class="cards_box">
        <AppMainCard v-for="card in store.characterList" :key="card.id" :details="card" />
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/variables' as*;

.cards_box {
    display: flex;
    flex-wrap: wrap;
}
</style>
