<script setup>
import FavoritePlace from '@/FavoritePlace/FavoritePlace.vue';
import IButton from '@/components/IButton.vue';
import { ref, reactive } from 'vue'

const buttonVariante = ref('gradient')

const changeButtonVariante = () => {
    buttonVariante.value = buttonVariante.value === 'gradient' ? 'outline' : 'gradient'
}
</script>

<template>
    <div class="px-6">
        <div class="text-gray mb-4">Додані маркери({{counter}})</div>   
        <FavoritePlace v-for="n in 4" :key="n" />
        <IButton class="w-full mt-10" :variant="buttonVariante" @click="increment">Додати маркери</IButton>
        <IButton class="w-full mt-10" @click="increment">Додати маркери</IButton>
    </div>
</template>