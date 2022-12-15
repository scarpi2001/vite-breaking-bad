<script >
import { store } from '../../store';

export default {
    name: "AppMainSelect",
    data() {
        return {
            store,
        }
    },
}
</script>

<template>
    <div class="select_container">
        <select name="" id="" @click="$emit('filter')" v-model="store.status">
            <option disabled>Seleziona status</option>
            <option value="Alive">Alive</option>
            <option value="Dead">Dead</option>
            <option value="Unknown">Unknown</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/variables' as*;

.select_container {
    max-width: 1200px;
    margin: 30px auto;
}
</style>
