<script>
import mainCard from "./AppMain-card.vue";
import mainSelect from  "./AppMain-select.vue";
import searchResults from "./AppMain-results.vue";

export default {
    name: 'AppMain',
    components: {
        mainCard,
        mainSelect,
        searchResults
    }
}
</script>

<template>
    <main>
        <mainSelect/>
        <div class="main-container w-75 m-auto pt-4">
            <searchResults/>
            <div class="row py-4 px-5">
                <mainCard/>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
.main-container {
    background-color: white;
    color: black;
}
</style>
