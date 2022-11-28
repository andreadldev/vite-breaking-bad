<script>
import Card from "./Card.vue";
export default {
    name: 'AppMain',
    components: {
        Card
    }
}
</script>

<template>
    <main>
        <div class="main-container w-75 my-5 m-auto d-flex">
            <div class="row py-4 px-5">
                <Card/>
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
