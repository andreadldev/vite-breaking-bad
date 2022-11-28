<script>
import axios from "axios";
export default {
    name: 'AppMain',

    data() {
        return {
            characters: []
        }
    },
    created() {
        axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
            this.characters = resp.data;
            console.log(this.characters);
            });
    }
}
    
</script>

<template>
    <main>
        <div class="main-container w-75 my-5 m-auto d-flex">
            <div class="row py-4 px-5">
                <div class="character col-3 p-3 text-center" v-for="character in characters">
                    <img src="https://via.placeholder.com/150" alt="...">
                    <div class="info pt-3">
                        <h4>{{character.name}}</h4>
                        <h5>{{character.category}}</h5>
                        <span class="fw-semibold">{{character.status}}</span>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
.main-container {
    background-color: white;
    color: black;
}

.character {
    background-color: var(--background);
    border: 10px solid white;
}

h4 {
    color: white;
}
</style>
