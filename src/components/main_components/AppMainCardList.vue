<script >
import axios from 'axios';
import AppMainCard from './AppMainCard.vue';

import { store } from './store.js';

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
    mounted() {
        axios.get(store.apiURL)
            .then(res => {
                store.characterList = res.data.results;
            })
            .catch(err => {
                console.log("Errori", err);
            }

            );
    }
}
</script>

<template>
    <!-- contenitore cards -->
    <div class="cards_box">
        <AppMainCard v-for="(card, index) in cards" :key="index" :details="card" />
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/variables' as*;

.cards_box {
    display: flex;
    flex-wrap: wrap;
}
</style>
