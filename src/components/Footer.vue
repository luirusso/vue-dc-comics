<template>
  <footer>
      
    <div class="footer-links">
        <div class="container">
            <div class="links">
                
                <div>
                    <ul>
                        <li>
                            <h2>DC COMICS</h2>
                        </li>
                        <li v-for="link in dcComicsLinks" :key="link">
                            <a href=""> {{ link.text }} </a>
                        </li>
                    </ul>

                    <ul>
                        <li>
                            <h2>SHOP</h2>
                        </li>
                        <li v-for="link in shopLinks" :key="link">
                            <a href=""> {{ link.text }} </a>
                        </li>
                    </ul>
                </div>

                <ul>
                    <li>
                        <h2>DC</h2>
                    </li>
                    <li v-for="link in dcLinks" :key="link">
                        <a href=""> {{ link.text }} </a>
                    </li>
                </ul>

                <ul>
                    <li>
                        <h2>SITES</h2>
                    </li>
                    <li v-for="link in dcSitesLinks" :key="link">
                        <a href=""> {{ link.text }} </a>
                    </li>
                </ul>
            </div>
            <div class="dc-logo-bg">
                    
            </div>
        </div>
    </div>
    <div class="footer-bottom">
        <div class="container bottom">
            <div class="sign-up">
                <div>
                    <button>
                        SIGN UP
                    </button>
                </div>
                <div class="follow-us">
                    <h2>
                        FOLLOW US
                    </h2>
                    <img src="../assets/footer-facebook.png" alt="">
                    <img src="../assets/footer-facebook.png" alt="">
                    <img src="../assets/footer-facebook.png" alt="">
                    <img src="../assets/footer-facebook.png" alt="">
                    <img src="../assets/footer-facebook.png" alt="">
                </div>
            </div>
        </div>
    </div>
  </footer>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return{
            dcComicsLinks: [
                {
                    text: 'Characters'
                },
                {
                    text: 'Comics'
                },
                {
                    text: 'Movies'
                },
                {
                    text: 'TV'
                },
                {
                    text: 'Games'
                },
                {
                    text: 'Videos'
                },
                {
                    text: 'News'
                },
            ],
            shopLinks: [
                {
                    text: 'Shop DC'
                },
                {
                    text: 'Shop DC Collectibles'
                },
            ],
            dcLinks: [
                {
                    text: 'Terms Of Use'
                },
                {
                    text: 'Privacy policy (New)'
                },
                {
                    text: 'Ad Choices'
                },
                {
                    text: 'Advertising'
                },
                {
                    text: 'Jobs'
                },
                {
                    text: 'Subscriptions'
                },
                {
                    text: 'Talent Workshops'
                },
                {
                    text: 'CPSC Certificates'
                },
                {
                    text: 'Ratings'
                },
                {
                    text: 'Shop Help'
                },
                {
                    text: 'Contact Us'
                },
            ],
            dcSitesLinks: [
                {
                    text: 'DC'
                },
                {
                    text: 'MAD Magazine'
                },
                {
                    text: 'DC Kids'
                },
                {
                    text: 'DC Universe'
                },
                {
                    text: 'DC Power Visa'
                },
            ],
        }
    }

}
</script>

<style lang="scss">
footer {


    a {
        color: lightgray;
    }

    ul {
        list-style: none;
        padding: 0 1rem;

        li {
            font-size: 12px;
            padding-bottom: 5px;
        }
    }

    .footer-links {
        background-image: url(../assets/footer-bg.jpg);
        background-size: cover;
        color: white;

        .container {
            display: flex;
            justify-content: space-between;
        }

        .links {
            display: flex;
            padding: 2rem 0;
        }

        h2 {
            padding: 1rem 0;
        }
    }

    .dc-logo-bg {
        background-image: url(../assets/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position-y: -83px;
        width: 100%;
        background-position-x: right;
    }

    .footer-bottom {
        height: 120px;
        background-color: #303030;

        .container.bottom {
            height: 120px;
        }

            
        .sign-up {
            display: flex;
            justify-content: space-between;
            height: 100%;
            align-items: center;
        }

        .follow-us {
            display: flex;
            justify-content: space-between;
        }
    }
}

</style>