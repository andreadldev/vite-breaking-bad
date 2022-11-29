<script>
import axios from "axios";
import { store } from '../store.js';

export default {
    name: 'Card',
    data() {
        return {
            characters: [],
            store
        }
    },
    created() {
        axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
            this.characters = resp.data;
            }
        );
    }
}
</script>

<template>
    <div class="character col-xl-3 col-lg-4 col-md-6 p-3 text-center" v-for="character in characters">
        <img class="w-100" :src=character.img alt="...">
        <div class="info pt-3">
            <h4>{{character.name}}</h4>
            <h5>{{character.category}}</h5>
            <span class="fw-semibold">{{character.status}}</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.character {
    background-color: var(--background);
    border: 10px solid white;
}

h4 {
    color: white;
}

img {
    width: 100%;
    height: 250px;
    object-fit: cover;
    object-position: 50% 0;
}
</style>