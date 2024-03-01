<script>
import AppEcommerce from './AppEcommerce.vue';

export default {
    data() {
        return {
            list1: ["Characters", "Comics", "Movies", "Tv", "Games", "Videos", "News"],
            list2: ["Shop DC", "Shop DC Collectibles"],
            list3: ["Terms of use", "Privacy policy(New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"],
            list4: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"],

            socialIcon: [
                "/img/footer-facebook.png",
                "/img/footer-twitter.png",
                "/img/footer-youtube.png",
                "/img/footer-pinterest.png",
                "/img/footer-periscope.png"
            ]
        }
    },
    components: {
        AppEcommerce,
    },
    name: 'AppFooter',
}

</script>

<template>
    <AppEcommerce></AppEcommerce>
    <div class="footer-container">
        <div class="footer">
            <div class="links">
                <div class="links-first-col">
                    <div class="links-list">
                        <h3>Dc comics</h3>
                        <ul>
                            <li v-for="item of list1">{{ item }}</li>
                        </ul>
                    </div>
                    <div class="links-list">
                        <h3>Shop</h3>
                        <ul>
                            <li v-for="item of list2">{{ item }}</li>
                        </ul>
                    </div>
                </div>
                <div class="links-second-col">
                    <div class="links-list">
                        <h3>DC</h3>
                        <ul>
                            <li v-for="item of list3">{{ item }}</li>
                        </ul>
                    </div>
                </div>
                <div class="links-third-col">
                    <div class="links-list">
                        <h3>SITES</h3>
                        <ul>
                            <li v-for="item of list4">
                                {{ item }}</li>

                        </ul>
                    </div>
                </div>
            </div>
            <img class="logo-footer" src="/img/dc-logo-bg.png" alt="">
        </div>
    </div>
    <div class="subfooter-container">
        <div class="sub-footer">
            <button class="signup-btn">Sign-up Now!</button>
            <div class="follow">
                <h4>Follow us</h4>
                <div class="social">
                    <img v-for="icon of socialIcon" :src="icon" alt="">

                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
@use '../src/styles/variables' as *;
@use '../src/styles/mixins' as *;

.footer-container {
    background-color: #1c1c1c;
    color: white;
    margin: auto;
    padding-top: 45px;
    padding-bottom: 60px;
    background-image: url(/img/footer-bg.jpg);
    background-size: cover;
    overflow: hidden;

    .footer {
        position: relative;
        width: 70%;
        margin: auto;

        .links {
            display: flex;

            gap: 50px;

            h3 {
                font-size: 20px;
                text-transform: uppercase;
                padding-bottom: 20px;
            }

            ul {

                li {
                    color: #959595;
                    padding-bottom: 5px;
                }
            }
        }

        .logo-footer {
            position: absolute;
            transform: scale(1.2);
            top: -70px;
            right: 0;
        }
    }

}

.subfooter-container {
    margin: auto;
    padding: 30px 0;
    background-color: #1c1c1c;
    position: relative;

    .sub-footer {
        // this mixin will give display flex, justify-content: center and width 70% properties to the container
        @include flex-container;

        .signup-btn {
            padding: 17px;
            border: 2px solid $primaryColor;
            background-color: transparent;
            color: white;
            text-transform: uppercase;
        }

        .follow {
            display: flex;
            align-items: center;
            gap: 20px;

            h4 {
                font-size: 20px;
                color: $primaryColor;
                text-transform: uppercase;
            }

            .social {
                display: flex;
                gap: 15px
            }
        }

    }

}
</style>