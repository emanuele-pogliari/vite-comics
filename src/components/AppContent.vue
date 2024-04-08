<script>
import ComicItem from './ComicItem.vue';
import comicsData from '../data/comicsData.js';

export default {
    name: 'AppContent',

    components: {
        ComicItem,
    },

    data() {
        return {
            comicsData: comicsData.comics
        }
    },
}
</script>

<template>
    <div class="content-container">
        <div class="jumbotron">
            <img src="/img/jumbotron.jpg" alt="">
            <div class="current-series">Current Series</div>
        </div>
        <div class="content">
            <ComicItem v-for="currentComic in comicsData" :comic="currentComic"></ComicItem>
            <button class="load-btn">Load More</button>
        </div>
    </div>
</template>

<style lang="scss">
@use '../src/styles/variables' as *;
@use '../src/styles/mixins' as *;


.jumbotron {
    position: relative;

    width: 100%;
    height: 400px;

    img {
        width: 100%;
        height: 100%;

        object-fit: cover;
        object-position: top;

    }

    .current-series {
        position: absolute;

        padding: 5px 30px;

        left: 270px;

        transform: translateY(-50%);

        font-family: 'Barlow Condensed', sans-serif;
        font-size: 30px;
        font-weight: 700;
        text-transform: uppercase;
        background-color: $primaryColor;

    }
}

.content-container {
    padding-bottom: 20px;

    background-color: #303030;
    color: white;


    .content {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 50px 25px;

        width: 70%;

        margin: auto;
        padding-top: 55px;

        font-size: 28px;

        .load-btn {
            display: block;
            justify-self: center;

            padding: 17px 60px;
            background-color: $primaryColor;
            border: 0;
            text-transform: uppercase;
            font-family: 'Barlow Condensed', sans-serif;
            color: #FFF;
            font-size: 18px;
            font-weight: bold;
        }
    }


}
</style>

