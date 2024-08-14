<script setup>
import Homepage from "./views/HomepageView.vue"
import FavoritePlaces from "./FavoritePlaces/FavoritePlaces.vue";
</script>

<template>
    <Homepage />
    <FavoritePlaces>
        <div>This is super slot</div>
        <template #list>This is list</template>
        <template #label>This is label</template>
    </FavoritePlaces>
</template>