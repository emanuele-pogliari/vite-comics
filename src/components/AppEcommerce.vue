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
                    name: "DC Merchandise",
                },

                {
                    image: "/img/buy-comics-subscriptions.png",
                    name: "Subscription",
                },

                {
                    image: "/img/buy-comics-shop-locator.png",
                    name: "Comic Shop Locator",
                },

                {
                    image: "/img/buy-dc-power-visa.svg",
                    name: "DC Power Visa",
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
@use '../src/styles/variables' as *;
@use '../src/styles/mixins' as *;

.ecommerce-container {
    padding-bottom: 50px;
    padding-top: 50px;

    background-color: $primaryColor;

    ul {
        // this mixin will give display flex, justify-content: center and width 70% properties to the container

        display: flex;
        justify-content: center;
        gap: 50px;
        align-items: center;
        margin: auto;
        width: 70%;

        padding: 0 45px;

        li {
            display: flex;
            align-items: center;
            gap: 20px;

            color: white;


            img {
                width: 50px;
            }

            p {
                font-size: 18px;
                font-weight: 500;
                text-transform: uppercase;
            }
        }

    }

}
</style>