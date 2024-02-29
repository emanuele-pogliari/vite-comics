<script>
export default {
    name: 'AppFooter',
}
</script>

<template>
    <div class="footer-container">
        <div class="footer">
            <div class="links">
                <div class="links-first-col">
                    <div class="links-list">
                        <h3>Dc Comics</h3>
                        <ul>
                            <li>Characters</li>
                            <li>Comics</li>
                            <li>Movies</li>
                            <li>Tv</li>
                            <li>Games</li>
                            <li>Videos</li>
                            <li>News</li>
                        </ul>
                    </div>
                    <div class="links-list">
                        <h3>Shop</h3>
                        <ul>
                            <li>Shop DC</li>
                            <li>Shop DC Collictibles</li>
                        </ul>
                    </div>
                </div>
                <div class="links-second-col">
                    <div class="links-list">
                        <h3>Dc</h3>
                        <ul>
                            <li>Terms of use</li>
                            <li>Privacy policy (New)</li>
                            <li>Ad Choices</li>
                            <li>Advertising</li>
                            <li>Jobs</li>
                            <li>Subscriptions</li>
                            <li>Talent Workshops</li>
                            <li>CPSC Certificates</li>
                            <li>Ratings</li>
                            <li>Shop Help</li>
                            <li>Contact Us</li>
                        </ul>
                    </div>
                </div>
                <div class="links-third-col">
                    <div class="links-list">
                        <h3>Sites</h3>
                        <ul>
                            <li>DC</li>
                            <li>MAD Magazine</li>
                            <li>DC Kids</li>
                            <li>DC Universe</li>
                            <li>DC Power Visa</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="subfooter-container">
        <div class="sub-footer">
            <button class="signup-btn">Sign-up Now!</button>
        </div>
    </div>
</template>

<style lang="scss">
.footer-container {
    background-color: #1c1c1c;
    color: white;
    margin: auto;
    padding-top: 45px;
    padding-bottom: 60px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;

    .footer {
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
                list-style-type: none;

                li {
                    color: #959595;
                    padding-bottom: 10px;
                }
            }
        }
    }
}

.subfooter-container {
    margin: auto;
    padding: 30px 0;
    background-color: #1c1c1c;

    .sub-footer {
        width: 70%;
        margin: auto;
    }

    .signup-btn {
        padding: 17px;
        border: 2px solid #0282F9;
        background-color: transparent;
        color: white;
        text-transform: uppercase;
    }
}
</style>