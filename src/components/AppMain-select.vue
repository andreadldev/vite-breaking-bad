<script>
import axios from "axios";
import { store } from '../store.js';

export default {
    name: "mainSelect",
    data() {
        return {
            store
        }
    },
    methods: {
        getCharacters() {
            if (this.store.category == "Breaking Bad") {
                this.store.characters = '';
                this.store.defaultSelect = false;
                axios.get("https://www.breakingbadapi.com/api/characters?category=Breaking+Bad").then((resp) => {
                this.store.characters = resp.data;
                    }
                );
            }
            else if (this.store.category == "Better Call Saul") {
                this.store.characters = '';
                this.store.defaultSelect = false;
                axios.get("https://www.breakingbadapi.com/api/characters?category=Better+Call+Saul").then((resp) => {
                this.store.characters = resp.data;
                    }
                );
            }
            else if (this.store.category == "All" && this.store.defaultSelect == false) {
                this.store.characters = '';
                axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
                this.store.characters = resp.data;
                    }
                );
            }
        }
    }
}
</script>

<template>
    <div>
        <select class="form-select w-25 my-3 mb-4" aria-label="Default select example" v-model="store.category" @change="this.getCharacters()">
            <option selected disabled>Select Category</option>
            <option value="Breaking Bad">Breaking Bad</option>
            <option value="Better Call Saul">Better Call Saul</option>
            <option value="All">All</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
select {
    margin-left: 12.5%;
}
</style>