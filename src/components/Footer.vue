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
                        <li v-for="(link, index) in dcComicsLinks" :key="`dcComicsLink-${index}`">
                            <a href=""> {{ link.text }} </a>
                        </li>
                    </ul>

                    <ul>
                        <li>
                            <h2>SHOP</h2>
                        </li>
                        <li v-for="(link, index) in shopLinks" :key="`shopLink-${index}`">
                            <a href=""> {{ link.text }} </a>
                        </li>
                    </ul>
                </div>

                <ul>
                    <li>
                        <h2>DC</h2>
                    </li>
                    <li v-for="(link, index) in dcLinks" :key="`dcLink-${index}`">
                        <a href=""> {{ link.text }} </a>
                    </li>
                </ul>

                <ul>
                    <li>
                        <h2>SITES</h2>
                    </li>
                    <li v-for="(link, index) in dcSitesLinks" :key="`dcSitesLink-${index}`">
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
                    <img src="../assets/footer-twitter.png" alt="">
                    <img src="../assets/footer-youtube.png" alt="">
                    <img src="../assets/footer-pinterest.png" alt="">
                    <img src="../assets/footer-periscope.png" alt="">
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
            font-size: 17px;
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

            button {
                display: flex;
                align-items: center;
                justify-content: center;
                height: 50px;
                width: 170px;
                border: 2px solid #0282F9;
                background: transparent;
                color: white;
                font-size: 30px;
                transition: background 0.3s;
                transition: box-shadow 0.3s;
                &:hover {
                    cursor: pointer;
                    background: #0282F9;
                    color: #303030;
                    box-shadow: 3px 3px 7px 0px black;
                    
                }
            }
        }

        .follow-us {
            display: flex;
            justify-content: space-between;
            align-items: center;
            h2 {
                padding: 0 1.3rem;
                color: #0282F9;
                font-size: 1.7rem;
            }

            img {
                margin: 0 0.5rem;
                opacity: 0.5;
                transition: opacity .3s;
                &:hover {
                    cursor: pointer;
                    opacity: 1;
                }
            }
        }
    }
}

</style>