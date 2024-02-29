<script>
export default {
    name: 'AppNav',
}
</script>

<template>
    <header>
        <nav class="nav-container">
            <img class="img-logo" src="../assets/img/dc-logo.png" alt="">
            <ul class="nav-links">
                <li>Characters</li>
                <li>Comics</li>
                <li>Movies</li>
                <li>Tv</li>
                <li>Games</li>
                <li>Collectibles</li>
                <li>Videos</li>
                <li>Fans</li>
                <li>News</li>
                <li>Show</li>
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