<script>

export default {
    data() {
        return {
            items: [
                {
                    image: "/img/buy-comics-digital-comics.png",
                    name: "Digital Comics",
                },

                {
                    image: "/img/buy-comics-merchandise.png",
                    name: "Digital Comics",
                },

                {
                    image: "/img/buy-comics-subscriptions.png",
                    name: "Digital Comics",
                },

                {
                    image: "/img/buy-comics-shop-locator.png",
                    name: "Digital Comics",
                },

                {
                    image: "/img/buy-dc-power-visa.svg",
                    name: "Digital Comics",
                },
            ],
        }
    }
}

</script>

<template>
    <div class="ecommerce-container">
        <ul>
            <li v-for="item in items">
                <img :src="item.image">
                <p>{{ item.name }}</p>
            </li>
        </ul>
    </div>
</template>

<style lang="scss">
.ecommerce-container {
    background-color: #0282F9;
    height: 200px
}
</style>