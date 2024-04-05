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
    }
    });
</script>


<template>
    <div>
        asdfasdff awdfasdfasdf
        <h2>{{ foodName }}</h2>
        <p>{{ foodDesc }}</p>
        <button>Favorite</button>
    </div>
</template>

<style>
    img {
        height: 1.5em;
        float: right;
    }
</style>      