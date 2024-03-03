<script>
export default {
    name: 'ComicItem',

    props:{
        comic: Object,
    }
}
</script>


<template>
    <div class="comic">
        <img :src="comic.thumb" :alt="comic.series">
        <h4>{{ comic.series }}</h4>
    </div>
</template>


<style lang="scss">
.comic {
    width: calc(100% / 6 - 25px / 6 * 5);

    img {
        width: 185px;
        height: 185px;
        object-fit: cover;
        object-position: top;
    }

    h4 {
        font-size: 16px;
        text-transform: uppercase;
        font-family: 'Barlow Condensed', sans-serif;
    }
}
</style>


