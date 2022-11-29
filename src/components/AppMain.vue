<script>
import mainCard from "./AppMain-card.vue";
import mainSelect from  "./AppMain-select.vue";
export default {
    name: 'AppMain',
    components: {
        mainCard,
        mainSelect
    }
}
</script>

<template>
    <main>
        <mainSelect/>
        <div class="main-container w-75 m-auto d-flex">
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
