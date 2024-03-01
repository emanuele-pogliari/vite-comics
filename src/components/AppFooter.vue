<script>
import AppEcommerce from './AppEcommerce.vue';

export default {
    data() {
        return {
            linkList: [
                {
                    title: 'dc comics',
                    links: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                },
                {
                    title: 'shop',
                    links: ['Shop DC', 'Shop DC Collectibles']
                },
                {
                    title: 'dc',
                    links: ['Terms of Use', 'Privacy Policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshop', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                },
                {
                    title: 'sites',
                    links: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                },
            ],

            socials: [
                {
                    name: 'facebook',
                    icon: '/img/footer-facebook.png'
                },
                {
                    name: 'twitter',
                    icon: '/img/footer-twitter.png'
                },
                {
                    name: 'youtube',
                    icon: '/img/footer-youtube.png'
                },
                {
                    name: 'pinterest',
                    icon: '/img/footer-pinterest.png'
                },
                {
                    name: 'periscope',
                    icon: '/img/footer-periscope.png'
                },
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
    <footer>
        <div class="footer-top">
            <div class="footer-container">

                <div class="links">
                    <div v-for="currentLinkList in linkList" class="links-list">
                        <h3>{{ currentLinkList.title }}</h3>
                        <ul>
                            <li v-for="item in currentLinkList.links">{{ item }}</li>
                        </ul>
                    </div>
                </div>
                <div class="logo-footer">
                    <img src="/img/dc-logo-bg.png" alt="">
                </div>

            </div>
        </div>


        <div class="subfooter-container">
            <div class="sub-footer">
                <button class="signup-btn">Sign-up Now!</button>
                <div class="follow">
                    <h4>Follow us</h4>
                    <div class="social">
                        <img v-for="social of socials" :src="social.icon" :alt="social.name">
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
@use '../src/styles/variables' as *;
@use '../src/styles/mixins' as *;

footer {

    .footer-top {
        height: 370px;

        background-image: url('/img/footer-bg.jpg');
        background-position: cover;

        overflow: hidden;



        .footer-container {
            @include flex-container;
            align-items: center;
            height: 100%;
            padding: 20px 0;
        }

        .links {
            display: flex;
            flex-flow: column wrap;
            align-content: flex-start;
            gap: 20px 30px;

            height: 100%;

            padding: 20px 0;

            h3 {
                text-transform: uppercase;
                font-size: 1.5em;
                font-family: 'Barlow Condensed', sans-serif;
                color: white;
                margin-bottom: 10px;
            }

            ul {

                color: #ccc;
                font-size: .9em;
            }
        }

    }

}

.subfooter-container {
    margin: auto;
    padding: 30px 0;
    background-color: #303030;
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
                text-transform: uppercase;
                font-size: 1.5em;
                font-family: 'Barlow Condensed', sans-serif;
                color: $primaryColor;
            }

            .social {
                display: flex;
                gap: 15px
            }
        }

    }

}
</style>