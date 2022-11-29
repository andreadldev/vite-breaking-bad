<script>
import { store } from '../store.js';

export default {
    name: "mainSelect",
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div>
        <select class="form-select w-25 my-3 mb-4" aria-label="Default select example" v-model="store.category">
            <option selected disabled>Select Category</option>
            <option value="1">Breaking Bad</option>
            <option value="2">Better Call Saul</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
select {
    margin-left: 12.5%;
}
</style>