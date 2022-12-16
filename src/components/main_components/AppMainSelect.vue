<script >
import { store } from '../../store';

export default {
    name: "AppMainSelect",
    data() {
        return {
            store,
        }
    },
    methods: {
        reset() {
            store.status = "";
            this.$emit('filterForStatus');
        }
    }
}
</script>

<template>
    <div class="select_container">
        <select class="select" @change="$emit('filterForStatus')" v-model="store.status">
            <option disabled>Seleziona status</option>
            <option value="Alive">Alive</option>
            <option value="Dead">Dead</option>
            <option value="Unknown">Unknown</option>
        </select>
        <button class="select button" @click="reset">Reset</button>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/variables' as*;

.select_container {
    max-width: 1200px;
    margin: 30px auto;

    .select {
        padding: 15px;
        border-radius: 10px;
        cursor: pointer;

        &:hover {
            border-color: $tertiary;
            background-color: rgb(238, 237, 237);
        }
    }

    .select.button {
        color: $secondary;
        background-color: $tertiary;
        margin-left: 15px;
    }
}
</style>
