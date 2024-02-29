<script>
export default {
    name: 'AppNav',

    data() {
        return {
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
            <ul class="nav-links">
                <li v-for="link in links">{{ link }}</li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss">
header {
    margin: auto;
}

.nav-container {
    display: flex;
    justify-content: space-between;
    width: 70%;
    margin: auto;
    padding: 15px;

    .nav-links {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        list-style-type: none;
        gap: 20px;
        text-transform: uppercase;
    }

    .img-logo {
        width: 80px;
    }
}
</style>