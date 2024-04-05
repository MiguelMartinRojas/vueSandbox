<script lang="js">
import { defineComponent } from 'vue';

export default defineComponent({
    props: ['foodName', 'foodDesc', 'isFavorite'],
    data() {
        return {
        foodIsFavorite: this.isFavorite
        };
    },
    methods: {
        toggleFavorite($event) {
        this.$emit('toggle-favorite', {name: this.foodName, x: $event.clientX, y: $event.clientY });
        }
    }
    });
</script>


<template>
    <div>
        asdfasdff awdfasdfasdf
        <h2>{{ foodName }}</h2>
        <p>{{ foodDesc }}</p>
        <button @click="toggleFavorite">Favorite</button>
    </div>
</template>

<style>
    img {
        height: 1.5em;
        float: right;
    }
</style>      