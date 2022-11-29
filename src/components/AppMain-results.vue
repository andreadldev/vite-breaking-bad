<script>
import { store } from '../store.js';

export default {
    name: 'Card',
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="mx-5 p-3" v-if="this.store.characters.length != 0 && this.store.defaultSelect == false">
        {{this.store.characters.length}} risultati
    </div>
</template>

<style lang="scss" scoped>
div {
    background-color: #212529;
    color: white;
    font-weight: bold;
}
</style>