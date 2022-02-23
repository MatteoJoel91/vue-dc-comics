<template>
    <header>
        <div class="contenitore">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>

            <nav>
                <ul>
                    <li v-for="link, i in links" :key="i">
                    <a :href="link.url" :class="link.active ? 'active' : ''">{{ link.text }}</a>
                    </li>
                </ul>
            </nav>
        </div>
        <div class="jumbo">
          
        </div>
    </header>  
</template>

<script>
export default {
    name: 'MyHeader',
    data(){
    return{
      links:[
        {
          "text": "CHARACTERS",
          "url": "#",
          "active": false
        },
        {
          "text": "COMICS",
          "url": "#",
          "active": true
        },
        {
          "text": "MOVIES",
          "url": "#",
          "active": false
        },
        {
          "text": "TV",
          "url": "#",
          "active": false
        },
        {
          "text": "GAMES",
          "url": "#",
          "active": false
        },
        {
          "text": "COLLECTIBLES",
          "url": "#",
          "active": false
        },
        {
          "text": "VIDEOS",
          "url": "#",
          "active": false
        },
        {
          "text": "FANS",
          "url": "#",
          "active": false
        },
        {
          "text": "NEWS",
          "url": "#",
          "active": false
        },
        {
          "text": "SHOP",
          "url": "#",
          "active": false
        },
        
      ]
    }
  }
}
</script>

<style scoped lang="scss">

  @import "../assets/style/variabili.scss";

  .contenitore{
    width: 70%;
    margin: auto;
    height: 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .logo{
      width: 80px;
      img{
        max-width: 100%;
      }
    }
    nav{
    
      li{
        display: inline-block;
        a{
          margin: 0 5px;
          text-decoration: none;
          color: $coloreBackgroundScuro;
          padding: 35px 5px;
          &.active{
            color: $coloreBlu;
            border-bottom: solid 6px $coloreBlu;
          }
          &:hover{
            color: $coloreBlu;
            border-bottom: solid 6px $coloreBlu;
          }
        }
      }
    }
  }
  .jumbo{
    background-image: url('../assets/img/jumbotron.jpg');
    background-repeat: no-repeat;
    height: 400px;
    width: 100%;
    background-size: cover;
  }
</style>