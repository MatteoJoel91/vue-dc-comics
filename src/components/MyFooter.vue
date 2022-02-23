<template>
    <footer>
        <div class="footer-up">
            <div class="contenitore-cards" v-for="card, i in cards" :key="i">
                <img :src="require(`../assets/img/${card.image}`)" alt="">
                <span>{{card.text}}</span>
            </div>
        </div>
        <div class="footer-mid">
            <div class="logo-bg">
                <img src="../assets/img/dc-logo-bg.png" alt="">
                <div class="link-footer">

                    <div class="collonna">
                        <h3>DC Comics</h3>
                        <div>
                            <ul>
                            <li><a href="#">Characters</a></li>
                            <li><a href="#">Comics</a></li>
                            <li><a href="#">Movies</a></li>
                            <li><a href="#">TV</a></li>
                            <li><a href="#">Games</a></li>
                            <li><a href="#">Videos</a></li>
                            <li><a href="#">News</a></li>
                            </ul>
                        </div>
                        <h3>Shop</h3>
                        <div>
                            <ul>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                            </ul>
                        </div>

                    </div>


                    <div class="collonna">
                        <h3>DC</h3>
                        <div>
                            <ul>
                            <li><a href="#">Terms of Use</a></li>
                            <li><a href="#">Privacy policy (New)</a></li>
                            <li><a href="#">Ad Choices</a></li>
                            <li><a href="#">Advertising</a></li>
                            <li><a href="#">Jobs</a></li>
                            <li><a href="#">Subscriptions</a></li>
                            <li><a href="#">Talent Workshops</a></li>
                            <li><a href="#">CPSC Certificates</a></li>
                            <li><a href="#">Ratings</a></li>
                            <li><a href="">Shop Help</a></li>
                            <li><a href="#">Contact Us</a></li>
                            </ul>
                        </div>
                    </div>

                    <div class="collonna">
                        <h3>Sites</h3>
                        <div>
                            <ul>
                            <li><a href="#">DC</a></li>
                            <li><a href="#">MAD Magazine</a></li>
                            <li><a href="#">DC Kids</a></li>
                            <li><a href="#">DC Universe</a></li>
                            <li><a href="#">DC Power Visa</a></li>
                            </ul>
                        </div>
                    </div>

                </div>

            </div>
            
        </div>
        <div class="footer-bot">
            <div class="contenitore-footer-bot">
                <button>SIGN-UP NOW!</button>
                <div class="social-footer">
                    <a href="#">FOLLOW US</a>
                    <img src="../assets/img/footer-facebook.png" alt="">
                    <img src="../assets/img/footer-twitter.png" alt="">
                    <img src="../assets/img/footer-youtube.png" alt="">
                    <img src="../assets/img/footer-pinterest.png" alt="">
                    <img src="../assets/img/footer-periscope.png" alt="">
                </div>
            </div>
            
        </div>
    </footer>
</template>

<script>
export default {
    name: 'MyFooter',
    data(){
    return{
      cards:[
        {
          "text": "DIGITAL COMICS",
          "image": "buy-comics-digital-comics.png"
        },
        {
          "text": "DC MERCHANDISE",
          "image": "buy-comics-merchandise.png"
        },
        {
          "text": "SUBSCRIPTIONS",
          "image": "buy-comics-subscriptions.png"
        },
        {
          "text": "COMIC SHOP LOCATOR",
          "image": "buy-comics-shop-locator.png"
        },
        {
          "text": "DC POWER VISA",
          "image": "buy-dc-power-visa.svg"
        },
      ]
    }
  },
}
</script>

<style scoped lang="scss">

    @import "../assets/style/variabili.scss";

    footer{
        width: 100%;
        background-color: $coloreBlu;

        .footer-up{
            width: 70%;
            height: 150px;
            display: flex;
            justify-content: center;
            margin: 0 auto;
            z-index: 90;
            position: relative;

            .contenitore-cards{
                display: flex;
                align-items: center;
                color: $coloreBianco;
                margin: 0 30px;
                padding: 0 5px;

                &:hover{
                    cursor: pointer;
                    background-color: $coloreBluHover;
                    border-radius: 20px;
                }
            }

            img{
            width: 50px;
            margin: 10px;
            }
        }
    }
        
        
        
    .footer-mid{
        width: 100%;
        background-image: url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        height: 450px;

        .logo-bg{
            position: relative;
            width: 70%;
            margin: 0 auto;
            img{
                position: absolute;
                right: 0px;
                top: - 60px;
                
            }
            .link-footer{
                display: flex;
                padding-top: 40px;
                .collonna{
                    margin-right: 15px;
                }

                h3{
                    color: $coloreBianco;
                    margin: 15px 0px;
                }
                ul{
                    list-style-type: none;
                }
                li{
                    padding: 5px 0px;
                }
                a{
                    color: $coloreGrigio;
                    text-decoration: none;
                    &:hover{
                        color: $coloreBlu;
                        cursor: pointer;
                    }
                }
            }
        }
    }
    .footer-bot{
        width: 100%;
        background-color: $coloregrigioScuro;
        height: 100px;
        z-index: 90;
        position: relative;
        display: flex;
        align-items: center;
        

        .contenitore-footer-bot{
            width: 70%;
            display: flex;
            margin: 0 auto;
            justify-content: space-between;
            button{
                background-color: $coloregrigioScuro;
                color: $coloreBianco;
                border: solid 2px $coloreBlu;
                padding: 10px 10px;

                &:hover{
                    background-color: $coloreGrigio;
                    cursor: pointer;
                }
            }
            .social-footer{
                display: flex;
                align-items: center;

                a{
                    color: $coloreBlu;
                    text-decoration: none;
                    margin-right: 10px;
                }
                img{
                    margin: 10px;
                }
            }
            
        }
    }
</style>