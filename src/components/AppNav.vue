<script>
export default {
    name: 'AppNav',

    data() {
        return {
            // data link navbar
            links: ["Characters", "Comics", "Movies", "Tv", "Games", "Collectibles", "Videos", "Fans", "News", "Shop"],

            activeLinkIndex: 1,
        }
    }
}
</script>

<template>
    <header>
        <nav class="nav-container">
            <img class="img-logo" src="/img/dc-logo.png" alt="">
            <!-- add data on page and assign class active to the element that will have index = activeIndex -->
            <ul class="nav-links">
                <li v-for="(link, index) in links" :class="index == activeLinkIndex ? 'active' : ''">{{ link }}</li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss">
// 
@use '../src/styles/variables' as *;
@use '../src/styles/mixins' as *;

header {
    margin: auto;
}

.nav-container {
    // this mixin will give display flex, justify-content: center and width 70% properties to the container
    @include flex-container;
    align-items: center;

    .nav-links {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        gap: 20px;
        text-transform: uppercase;

        li {
            padding-top: 50px;
            padding-bottom: 50px;

            &.active {
                padding-bottom: 45px;
                border-bottom: 5px solid $primaryColor;
            }
        }
    }

    .img-logo {
        width: 80px;
    }
}
</style>