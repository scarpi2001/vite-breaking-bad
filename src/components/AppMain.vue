<script >
import axios from 'axios';
import AppMainSelect from './main_components/AppMainSelect.vue';
import AppMainTop from './main_components/AppMainTop.vue';
import AppMainCardList from './main_components/AppMainCardList.vue';

import { store } from '../store';

export default {
    name: "AppMain",
    components: {
        AppMainSelect,
        AppMainTop,
        AppMainCardList,
    },
    data() {
        return {
            store,
        }
    },
    methods: {
        getCards() {

            let myUrl = store.apiURL;

            if (store.status !== "") {
                myUrl += `?${store.apiStatus}=${store.status}`
            }
            axios.get(myUrl)
                .then(res => {
                    store.characterList = res.data.results;
                })
                .catch(err => {
                    console.log("Errori", err);
                }

                );
        }
    },
    mounted() {
        this.getCards();
    }
}
</script>

<template>
    <!-- select per stato -->
    <AppMainSelect @filter="getCards" />
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
    margin: 20px auto;
    padding: 30px;
    background-color: $secondary;
}
</style>
